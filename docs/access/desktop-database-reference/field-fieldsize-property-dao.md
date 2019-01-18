---
title: Propriedade Field.FieldSize (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 68a1b354b27515dd855703b9bf6344e4a9e90d7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712789"
---
# <a name="fieldfieldsize-property-dao"></a><span data-ttu-id="843dd-102">Propriedade Field.FieldSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="843dd-102">Field.FieldSize property (DAO)</span></span>


<span data-ttu-id="843dd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="843dd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="843dd-104">Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary **[Field](field-object-dao.md)** na coleção **[Fields](fields-collection-dao.md)** de um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="843dd-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="843dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="843dd-105">Syntax</span></span>

<span data-ttu-id="843dd-106">*expressão* . Tamanho do campo</span><span class="sxs-lookup"><span data-stu-id="843dd-106">*expression* .FieldSize</span></span>

<span data-ttu-id="843dd-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="843dd-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="843dd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="843dd-108">Remarks</span></span>

<span data-ttu-id="843dd-109">Você pode usar **FieldSize** com os métodos **[AppendChunk](field-appendchunk-method-dao.md)** e **[GetChunk](field-getchunk-method-dao.md)** para manipular campos grandes.</span><span class="sxs-lookup"><span data-stu-id="843dd-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="843dd-110">Como o tamanho de um campo Long Binary ou Memo pode exceder 64K, você deverá atribuir o valor retornado pelo **FieldSize** a uma variável grande o suficiente para armazenar uma variável **Long**.</span><span class="sxs-lookup"><span data-stu-id="843dd-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="843dd-111">Para determinar o tamanho de um objeto **Field** diferente dos tipos Memo e Long Binary, use a propriedade **[Size](field-size-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="843dd-111">To determine the size of a **Field** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="843dd-112">Se o servidor do banco de dados ou o driver ODBC não oferecer suporte aos cursores do servidor.</span><span class="sxs-lookup"><span data-stu-id="843dd-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="843dd-113">Se você estiver utilizando a biblioteca de cursor ODBC (isto é, a propriedade **DefaultCursorDriver** está definida como **dbUseODBC** ou como **dbUseDefault** quando o servidor não aceita cursores do lado do servidor).</span><span class="sxs-lookup"><span data-stu-id="843dd-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="843dd-114">Se você estiver usando uma consulta sem cursor (isto é, a propriedade **DefaultCursorDriver** está definida como **dbUseNoCursor**).</span><span class="sxs-lookup"><span data-stu-id="843dd-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="843dd-p101">A propriedade **FieldSize** e as funções VBA **Len()** ou **LenB()** podem retornar valores diferentes como o comprimento da mesma cadeia. As cadeias estão armazenadas no banco de dados do Microsoft Access em um formulário MBCS (Conjunto de Caracteres de Bytes Múltiplos), mas expostas por meio do VBA no formato Unicode. Como resultado, a função **Len()** retornará sempre o número de caracteres, a função **LenB** retornará sempre o número de caracteres X 2 (o Unicode usa dois bytes para cada caractere), mas **FieldSize** retornará alguns valores intermediários, se a sequência tiver caracteres MBCS. Por exemplo, fornecida uma cadeia composta de três caracteres normais e dois caracteres MBCS, **Len()** retornará 5, **LenB()** retornará 10 e **FieldSize** retornará 7, a soma de 1 para cada caractere normal e 2 para cada caractere MBCS.</span><span class="sxs-lookup"><span data-stu-id="843dd-p101">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string. Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format. As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters. For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="843dd-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="843dd-119">Example</span></span>

<span data-ttu-id="843dd-120">Este exemplo usa a propriedade **FieldSize** para listar o número de bytes usados pelos objetos Field Memo e Long Binary em duas tabelas diferentes.</span><span class="sxs-lookup"><span data-stu-id="843dd-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

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

<span data-ttu-id="843dd-p102">Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="843dd-p102">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
