---
title: Propriedade Field. FieldSize (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 68a1b354b27515dd855703b9bf6344e4a9e90d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293109"
---
# <a name="fieldfieldsize-property-dao"></a>Propriedade Field. FieldSize (DAO)


**Aplica-se ao:** Access 2013, Office 2013


Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary **[Field](field-object-dao.md)** na coleção **[Fields](fields-collection-dao.md)** de um objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . FieldSize

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Você pode usar **FieldSize** com os métodos **[AppendChunk](field-appendchunk-method-dao.md)** e **[GetChunk](field-getchunk-method-dao.md)** para manipular campos grandes.

Como o tamanho de um campo Long Binary ou Memo pode exceder 64K, você deverá atribuir o valor retornado pelo **FieldSize** a uma variável grande o suficiente para armazenar uma variável **Long**.

Para determinar o tamanho de um objeto **Field** diferente dos tipos Memo e Long Binary, use a propriedade **[Size](field-size-property-dao.md)**.

  - Se o servidor do banco de dados ou o driver ODBC não oferecer suporte aos cursores do servidor.

  - Se você estiver utilizando a biblioteca de cursor ODBC (isto é, a propriedade **DefaultCursorDriver** está definida como **dbUseODBC** ou como **dbUseDefault** quando o servidor não aceita cursores do lado do servidor).

  - Se você estiver usando uma consulta sem cursor (isto é, a propriedade **DefaultCursorDriver** está definida como **dbUseNoCursor**).

A propriedade **FieldSize** e as funções VBA **Len()** ou **LenB()** podem retornar valores diferentes como o comprimento da mesma cadeia. As cadeias estão armazenadas no banco de dados do Microsoft Access em um formulário MBCS (Conjunto de Caracteres de Bytes Múltiplos), mas expostas por meio do VBA no formato Unicode. Como resultado, a função **Len()** retornará sempre o número de caracteres, a função **LenB** retornará sempre o número de caracteres X 2 (o Unicode usa dois bytes para cada caractere), mas **FieldSize** retornará alguns valores intermediários, se a sequência tiver caracteres MBCS. Por exemplo, fornecida uma cadeia composta de três caracteres normais e dois caracteres MBCS, **Len()** retornará 5, **LenB()** retornará 10 e **FieldSize** retornará 7, a soma de 1 para cada caractere normal e 2 para cada caractere MBCS.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **FieldSize** para listar o número de bytes usados pelos objetos Field Memo e Long Binary em duas tabelas diferentes.

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
