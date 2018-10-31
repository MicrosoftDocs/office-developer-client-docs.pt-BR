---
title: EditModeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 790d28fa1efec5d5ad212094cb75f9d8d6456dbe
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860270"
---
# <a name="editmodeenum"></a><span data-ttu-id="a82d5-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="a82d5-102">EditModeEnum</span></span>

<span data-ttu-id="a82d5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a82d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a82d5-104">Especifica o status de edição de um registro.</span><span class="sxs-lookup"><span data-stu-id="a82d5-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a82d5-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a82d5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a82d5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a82d5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a82d5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a82d5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a82d5-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="a82d5-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="a82d5-109">0</span><span class="sxs-lookup"><span data-stu-id="a82d5-109">0</span></span></p></td>
<td><p><span data-ttu-id="a82d5-110">Indica que nenhuma operação de edição está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a82d5-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a82d5-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="a82d5-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="a82d5-112">1</span><span class="sxs-lookup"><span data-stu-id="a82d5-112">1</span></span></p></td>
<td><p><span data-ttu-id="a82d5-113">Indica que os dados no registro atual foram modificados, mas não foram salvos.</span><span class="sxs-lookup"><span data-stu-id="a82d5-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a82d5-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="a82d5-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="a82d5-115">2</span><span class="sxs-lookup"><span data-stu-id="a82d5-115">2</span></span></p></td>
<td><p><span data-ttu-id="a82d5-116">Indica que o método <a href="addnew-method-ado.md">AddNew</a> foi chamado e o registro atual no buffer de cópias é um novo registro que não foi salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a82d5-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a82d5-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="a82d5-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="a82d5-118">4</span><span class="sxs-lookup"><span data-stu-id="a82d5-118">4</span></span></p></td>
<td><p><span data-ttu-id="a82d5-119">Indica que o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="a82d5-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a82d5-120">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a82d5-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="a82d5-121">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a82d5-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a82d5-122">Constante</span><span class="sxs-lookup"><span data-stu-id="a82d5-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a82d5-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="a82d5-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a82d5-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="a82d5-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a82d5-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="a82d5-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a82d5-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="a82d5-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

