---
title: Método Field.GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c7eabceb1f7c130e349428aeb6b2dc079fe4319d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703745"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="b0886-102">Método Field.GetChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0886-102">Field.GetChunk method (DAO)</span></span>

<span data-ttu-id="b0886-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0886-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0886-104">Retorna o conteúdo no todo ou em parte de um objeto \*\*\*\*Field\*\*\*\* [Memo](field-object-dao.md) ou **Long Binary** na coleção **[Fields](fields-collection-dao.md)** de um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b0886-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0886-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0886-105">Syntax</span></span>

<span data-ttu-id="b0886-106">*expressão* . GetChunk (***deslocamento***, ***Bytes***)</span><span class="sxs-lookup"><span data-stu-id="b0886-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="b0886-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="b0886-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0886-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0886-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0886-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b0886-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b0886-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="b0886-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b0886-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b0886-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b0886-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0886-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0886-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="b0886-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="b0886-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0886-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b0886-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b0886-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b0886-116">O número de bytes a serem ignorados antes da cópia começar.</span><span class="sxs-lookup"><span data-stu-id="b0886-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0886-117"><em>Bytes</em></span><span class="sxs-lookup"><span data-stu-id="b0886-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="b0886-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0886-118">Required</span></span></p></td>
<td><p><span data-ttu-id="b0886-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b0886-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b0886-120">O número de bytes que você deseja retornar.</span><span class="sxs-lookup"><span data-stu-id="b0886-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b0886-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0886-121">Return value</span></span>

<span data-ttu-id="b0886-122">Variant</span><span class="sxs-lookup"><span data-stu-id="b0886-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="b0886-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0886-123">Remarks</span></span>

<span data-ttu-id="b0886-p101">Os bytes retornados por **GetChunk** são atribuídos à variável. Use **GetChunk** para retornar uma porção do valor de dados total de cada vez. Você pode usar o método **[AppendChunk](field-appendchunk-method-dao.md)** para remontar as peças.</span><span class="sxs-lookup"><span data-stu-id="b0886-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="b0886-127">Se offset for 0, **GetChunk** começará a copiar do primeiro byte do campo.</span><span class="sxs-lookup"><span data-stu-id="b0886-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="b0886-128">Se numbytes for maior que o número de bytes em um campo, **GetChunk** retornará o número real de bytes restantes no campo.</span><span class="sxs-lookup"><span data-stu-id="b0886-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="b0886-p102">[!OBSERVAçãO] Use um campo **Memo** para texto e coloque apenas dados binários em campos **Long Binary**. De outra forma, serão gerados resultados indesejados.</span><span class="sxs-lookup"><span data-stu-id="b0886-p102">Use a **Memo** field for text, and put binary data only in **Long Binary** fields. Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="b0886-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0886-131">Example</span></span>

<span data-ttu-id="b0886-p103">Este exemplo usa os métodos **AppendChunk** e **GetChunk** para preencher um campo de um objeto OLE com dados de outro registro, 32K de cada vez. Em um aplicativo real, convém usar um procedimento como este para copiar o registro de um empregado (inclusive a foto do empregado) de uma tabela para outra. Neste exemplo, o registro está simplesmente sendo copiado de volta para a mesma tabela. Observe que toda a manipulação das partes ocorre dentro de uma única sequência AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="b0886-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
