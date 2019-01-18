---
title: Método Field.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1ce1c359582194ce87dfaf4f409be4303486e09
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712656"
---
# <a name="fieldappendchunk-method-dao"></a>Método Field.AppendChunk (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Acrescenta dados de uma expressão de cadeia de caracteres a um objeto **[Field](field-object-dao.md)** Memo ou Long Binary em um **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . AppendChunk (***Val***)

*expressão* Uma variável que representa um objeto **Field** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Val</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma expressão ou variável Variant (subtipo String) que contém os dados para acrescentar ao objeto <strong>Field</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar os métodos **AppendChunk** e **[GetChunk](field-getchunk-method-dao.md)** para acessar subconjuntos de dados em um campo Memo ou Long Binary.

Você também pode usar esses métodos para poupar espaço de cadeia de caracteres quando trabalhar com campos Memo e Long Binary. Certas operações (copiar, por exemplo) envolvem cadeias de caracteres temporárias. Se o espaço de cadeia de caracteres for limitado, convém trabalhar com porções de um campo em vez de um campo inteiro.

Se não houver um registro atual quando você usar **AppendChunk**, ocorrerá um erro.

> [!NOTE]
> A operação inicial **AppendChunk** (após uma chamada **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)** ) simplesmente colocará os dados no campo, sobrescrevendo quaisquer dados existentes. Chamadas subsequentes **AppendChunk** na mesma sessão **Edit** ou **AddNew** adicionarão dados aos já existentes.

## <a name="example"></a>Exemplo

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
