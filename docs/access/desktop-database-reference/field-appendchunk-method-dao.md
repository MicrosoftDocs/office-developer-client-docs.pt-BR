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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293165"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="a3612-102">Método Field.AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3612-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="a3612-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3612-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3612-104">Acrescenta dados de uma expressão de cadeia de caracteres a um objeto **[Field](field-object-dao.md)** Memo ou Long Binary em um **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="a3612-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3612-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3612-105">Syntax</span></span>

<span data-ttu-id="a3612-106">*expressão* . AppendChunk(***Val***)</span><span class="sxs-lookup"><span data-stu-id="a3612-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="a3612-107">*expressão* Uma variável que representa um objeto de **Campo**.</span><span class="sxs-lookup"><span data-stu-id="a3612-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3612-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3612-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3612-109">Nome</span><span class="sxs-lookup"><span data-stu-id="a3612-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3612-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="a3612-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a3612-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a3612-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a3612-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3612-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3612-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="a3612-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="a3612-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3612-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3612-115"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="a3612-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a3612-116">Uma expressão ou variável Variant (subtipo String) que contém os dados para acrescentar ao objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3612-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3612-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3612-117">Remarks</span></span>

<span data-ttu-id="a3612-118">Você pode usar os métodos **AppendChunk** e **[GetChunk](field-getchunk-method-dao.md)** para acessar subconjuntos de dados em um campo Memo ou Long Binary.</span><span class="sxs-lookup"><span data-stu-id="a3612-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="a3612-p101">Você também pode usar esses métodos para poupar espaço de cadeia de caracteres quando trabalhar com campos Memo e Long Binary. Certas operações (copiar, por exemplo) envolvem cadeias de caracteres temporárias. Se o espaço de cadeia de caracteres for limitado, convém trabalhar com porções de um campo em vez de um campo inteiro.</span><span class="sxs-lookup"><span data-stu-id="a3612-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="a3612-122">Se não houver um registro atual quando você usar **AppendChunk**, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="a3612-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="a3612-p102">A operação inicial **AppendChunk** (após uma chamada **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)** ) simplesmente colocará os dados no campo, sobrescrevendo quaisquer dados existentes. Chamadas subsequentes **AppendChunk** na mesma sessão **Edit** ou **AddNew** adicionarão dados aos já existentes.</span><span class="sxs-lookup"><span data-stu-id="a3612-p102">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data. Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="a3612-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a3612-125">Example</span></span>

<span data-ttu-id="a3612-p103">Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="a3612-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
