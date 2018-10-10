---
title: Método Field2.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: 540cd02d-1fc6-81d1-ac08-1e3df72a7208
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194088(v=office.15)
ms:contentKeyID: 48544886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052867
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 940181b26cee8ebe0cf6577385b911a28a962069
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463420"
---
# <a name="field2appendchunk-method-dao"></a><span data-ttu-id="e8af9-102">Método Field2.AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8af9-102">Field2.AppendChunk Method (DAO)</span></span>


<span data-ttu-id="e8af9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8af9-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e8af9-104">Acrescenta dados de uma expressão de cadeia de caracteres em um objeto **Field2** Memo ou Long Binary em um **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e8af9-104">Appends data from a string expression to a Memo or Long Binary **Field2** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8af9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8af9-105">Syntax</span></span>

<span data-ttu-id="e8af9-106">*expressão* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="e8af9-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="e8af9-107">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="e8af9-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="e8af9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8af9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8af9-109">Nome</span><span class="sxs-lookup"><span data-stu-id="e8af9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e8af9-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="e8af9-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="e8af9-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e8af9-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="e8af9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8af9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8af9-113">Val</span><span class="sxs-lookup"><span data-stu-id="e8af9-113">Val</span></span></p></td>
<td><p><span data-ttu-id="e8af9-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e8af9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e8af9-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e8af9-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e8af9-116">Uma expressão ou variável Variant (subtipo String) que contém os dados para acrescentar ao objeto <strong>Field2</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8af9-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field2</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e8af9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8af9-117">Remarks</span></span>

<span data-ttu-id="e8af9-118">Você pode usar os métodos **AppendChunk** e **GetChunk** para acessar subconjuntos de dados em um campo Memo ou Long Binary.</span><span class="sxs-lookup"><span data-stu-id="e8af9-118">You can use the **AppendChunk** and **GetChunk** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="e8af9-p101">Você também pode usar esses métodos para poupar espaço de cadeia de caracteres quando trabalhar com campos Memo e Long Binary. Certas operações (copiar, por exemplo) envolvem cadeias de caracteres temporárias. Se o espaço de cadeia de caracteres for limitado, convém trabalhar com porções de um campo em vez de um campo inteiro.</span><span class="sxs-lookup"><span data-stu-id="e8af9-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="e8af9-122">Se não houver um registro atual quando você usar **AppendChunk**, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="e8af9-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e8af9-p102">A operação inicial <STRONG>AppendChunk</STRONG> (após uma chamada <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> ou <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> ) simplesmente colocará os dados no campo, sobrescrevendo quaisquer dados existentes. Chamadas subsequentes <STRONG>AppendChunk</STRONG> na mesma sessão <STRONG>Edit</STRONG> ou <STRONG>AddNew</STRONG> adicionarão dados aos já existentes.</span><span class="sxs-lookup"><span data-stu-id="e8af9-p102">The initial <STRONG>AppendChunk</STRONG> operation (after an <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> call) will simply place the data in the field, overwriting any existing data. Subsequent <STRONG>AppendChunk</STRONG> calls within the same <STRONG>Edit</STRONG> or <STRONG>AddNew</STRONG> session will then add to the existing data.</span></span></P>



## <a name="example"></a><span data-ttu-id="e8af9-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e8af9-125">Example</span></span>

<span data-ttu-id="e8af9-p103">Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="e8af9-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
     
    Function CopyLargeField(fldSource As Field2, _ 
       fldDestination As Field2) 
     
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
