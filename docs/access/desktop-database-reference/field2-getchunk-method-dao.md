---
title: Método Campo2. getChunk (DAO)
TOCTitle: GetChunk method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a4b850658ca4ab36b0d4f4cbed7266d39b4ff8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292773"
---
# <a name="field2getchunk-method-dao"></a><span data-ttu-id="9565f-102">Método Campo2. getChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="9565f-102">Field2.GetChunk method (DAO)</span></span>

<span data-ttu-id="9565f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9565f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9565f-104">Retorna todo ou parte do conteúdo de um objeto **Memo** ou **Long BinaryField2** na coleção Fields **[](fields-collection-dao.md)** de um objeto **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9565f-104">Returns all or a portion of the contents of a **Memo** or **Long BinaryField2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9565f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9565f-105">Syntax</span></span>

<span data-ttu-id="9565f-106">*expressão* . GetChunk (***deslocamento***, ***bytes***)</span><span class="sxs-lookup"><span data-stu-id="9565f-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="9565f-107">*expressão* Uma variável que representa um objeto **campo2** .</span><span class="sxs-lookup"><span data-stu-id="9565f-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9565f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9565f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9565f-109">Nome</span><span class="sxs-lookup"><span data-stu-id="9565f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9565f-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="9565f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9565f-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9565f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9565f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9565f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9565f-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="9565f-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="9565f-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9565f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9565f-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="9565f-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="9565f-116">O número de bytes a serem ignorados antes da cópia começar.</span><span class="sxs-lookup"><span data-stu-id="9565f-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9565f-117"><em>Bytes</em></span><span class="sxs-lookup"><span data-stu-id="9565f-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="9565f-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9565f-118">Required</span></span></p></td>
<td><p><span data-ttu-id="9565f-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="9565f-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="9565f-120">O número de bytes que você deseja retornar.</span><span class="sxs-lookup"><span data-stu-id="9565f-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="9565f-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9565f-121">Return value</span></span>

<span data-ttu-id="9565f-122">Variant</span><span class="sxs-lookup"><span data-stu-id="9565f-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="9565f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9565f-123">Remarks</span></span>

<span data-ttu-id="9565f-p101">Os bytes retornados por **GetChunk** são atribuídos à variável. Use **GetChunk** para retornar uma porção do valor de dados total de cada vez. Você pode usar o método **[AppendChunk](field-appendchunk-method-dao.md)** para remontar as peças.</span><span class="sxs-lookup"><span data-stu-id="9565f-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="9565f-127">Se offset for 0, **GetChunk** começará a copiar do primeiro byte do campo.</span><span class="sxs-lookup"><span data-stu-id="9565f-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="9565f-128">Se numBytes for maior do que o número de bytes no campo, **GetChunk** retornará o número real de bytes restantes no campo.</span><span class="sxs-lookup"><span data-stu-id="9565f-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="9565f-129">[!OBSERVAçãO] Use um campo **Memo** para texto e coloque apenas dados binários em campos **Long Binary**.</span><span class="sxs-lookup"><span data-stu-id="9565f-129">Use a **Memo** field for text, and put binary data only in **Long Binary** fields.</span></span> <span data-ttu-id="9565f-130">De outra forma, serão gerados resultados indesejados.</span><span class="sxs-lookup"><span data-stu-id="9565f-130">Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="9565f-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9565f-131">Example</span></span>

<span data-ttu-id="9565f-p103">Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="9565f-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
