---
title: EditModeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f2c93f652b76948439cd7f4571608f538155724b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881332"
---
# <a name="editmodeenum"></a><span data-ttu-id="07f59-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="07f59-102">EditModeEnum</span></span>

<span data-ttu-id="07f59-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="07f59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07f59-104">Especifica o status de edição de um registro.</span><span class="sxs-lookup"><span data-stu-id="07f59-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07f59-105">Constante</span><span class="sxs-lookup"><span data-stu-id="07f59-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="07f59-106">Valor</span><span class="sxs-lookup"><span data-stu-id="07f59-106">Value</span></span></p></th>
<th><p><span data-ttu-id="07f59-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="07f59-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07f59-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="07f59-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="07f59-109">0</span><span class="sxs-lookup"><span data-stu-id="07f59-109">0</span></span></p></td>
<td><p><span data-ttu-id="07f59-110">Indica que nenhuma operação de edição está em andamento.</span><span class="sxs-lookup"><span data-stu-id="07f59-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f59-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="07f59-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="07f59-112">1</span><span class="sxs-lookup"><span data-stu-id="07f59-112">1</span></span></p></td>
<td><p><span data-ttu-id="07f59-113">Indica que os dados no registro atual foram modificados, mas não foram salvos.</span><span class="sxs-lookup"><span data-stu-id="07f59-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07f59-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="07f59-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="07f59-115">2</span><span class="sxs-lookup"><span data-stu-id="07f59-115">2</span></span></p></td>
<td><p><span data-ttu-id="07f59-116">Indica que o método <a href="addnew-method-ado.md">AddNew</a> foi chamado e o registro atual no buffer de cópias é um novo registro que não foi salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="07f59-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f59-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="07f59-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="07f59-118">4</span><span class="sxs-lookup"><span data-stu-id="07f59-118">4</span></span></p></td>
<td><p><span data-ttu-id="07f59-119">Indica que o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="07f59-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="07f59-120">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="07f59-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="07f59-121">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="07f59-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07f59-122">Constante</span><span class="sxs-lookup"><span data-stu-id="07f59-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07f59-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="07f59-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f59-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="07f59-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07f59-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="07f59-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f59-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="07f59-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

