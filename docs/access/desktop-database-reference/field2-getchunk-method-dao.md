---
title: Método Field2.GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39501d9f39c1275e9020ee228ec2ec0a4169f40f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465139"
---
# <a name="field2getchunk-method-dao"></a><span data-ttu-id="4cdff-102">Método Field2.GetChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="4cdff-102">Field2.GetChunk Method (DAO)</span></span>


<span data-ttu-id="4cdff-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cdff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4cdff-104">Retorna todo ou parte do conteúdo de um objeto **Memo** ou **Long BinaryField2** na coleção **[Fields](fields-collection-dao.md)** de um objeto **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4cdff-104">Returns all or a portion of the contents of a **Memo** or **Long BinaryField2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cdff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cdff-105">Syntax</span></span>

<span data-ttu-id="4cdff-106">*expressão* . GetChunk (***deslocamento***, ***Bytes***)</span><span class="sxs-lookup"><span data-stu-id="4cdff-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="4cdff-107">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="4cdff-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="4cdff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cdff-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cdff-109">Nome</span><span class="sxs-lookup"><span data-stu-id="4cdff-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4cdff-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="4cdff-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="4cdff-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4cdff-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="4cdff-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cdff-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-113">Offset</span><span class="sxs-lookup"><span data-stu-id="4cdff-113">Offset</span></span></p></td>
<td><p><span data-ttu-id="4cdff-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4cdff-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4cdff-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4cdff-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4cdff-116">O número de bytes a serem ignorados antes da cópia começar.</span><span class="sxs-lookup"><span data-stu-id="4cdff-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cdff-117">Bytes</span><span class="sxs-lookup"><span data-stu-id="4cdff-117">Bytes</span></span></p></td>
<td><p><span data-ttu-id="4cdff-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4cdff-118">Required</span></span></p></td>
<td><p><span data-ttu-id="4cdff-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4cdff-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4cdff-120">O número de bytes que você deseja retornar.</span><span class="sxs-lookup"><span data-stu-id="4cdff-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4cdff-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4cdff-121">Return Value</span></span>

<span data-ttu-id="4cdff-122">Variant</span><span class="sxs-lookup"><span data-stu-id="4cdff-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdff-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cdff-123">Remarks</span></span>

<span data-ttu-id="4cdff-p101">Os bytes retornados por **GetChunk** são atribuídos à variável. Use **GetChunk** para retornar uma porção do valor de dados total de cada vez. Você pode usar o método **[AppendChunk](field-appendchunk-method-dao.md)** para remontar as peças.</span><span class="sxs-lookup"><span data-stu-id="4cdff-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="4cdff-127">Se offset for 0, **GetChunk** começará a copiar do primeiro byte do campo.</span><span class="sxs-lookup"><span data-stu-id="4cdff-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="4cdff-128">Se numbytes for maior que o número de bytes em um campo, **GetChunk** retornará o número real de bytes restantes no campo.</span><span class="sxs-lookup"><span data-stu-id="4cdff-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4cdff-p102">[!OBSERVAçãO] Use um campo <STRONG>Memo</STRONG> para texto e coloque apenas dados binários em campos <STRONG>Long Binary</STRONG>. De outra forma, serão gerados resultados indesejados.</span><span class="sxs-lookup"><span data-stu-id="4cdff-p102">Use a <STRONG>Memo</STRONG> field for text, and put binary data only in <STRONG>Long Binary</STRONG> fields. Doing otherwise will cause undesirable results.</span></span></P>



## <a name="example"></a><span data-ttu-id="4cdff-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4cdff-131">Example</span></span>

<span data-ttu-id="4cdff-p103">Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="4cdff-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
