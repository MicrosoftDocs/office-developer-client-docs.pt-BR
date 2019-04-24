---
title: EditModeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293578"
---
# <a name="editmodeenum"></a><span data-ttu-id="c88bd-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="c88bd-102">EditModeEnum</span></span>

<span data-ttu-id="c88bd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c88bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c88bd-104">Especifica o status de edição de um registro.</span><span class="sxs-lookup"><span data-stu-id="c88bd-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c88bd-105">Constant</span><span class="sxs-lookup"><span data-stu-id="c88bd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c88bd-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c88bd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c88bd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c88bd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c88bd-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="c88bd-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="c88bd-109">,0</span><span class="sxs-lookup"><span data-stu-id="c88bd-109">0</span></span></p></td>
<td><p><span data-ttu-id="c88bd-110">Indica que nenhuma operação de edição está em andamento.</span><span class="sxs-lookup"><span data-stu-id="c88bd-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88bd-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="c88bd-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="c88bd-112">1</span><span class="sxs-lookup"><span data-stu-id="c88bd-112">1</span></span></p></td>
<td><p><span data-ttu-id="c88bd-113">Indica que os dados no registro atual foram modificados, mas não foram salvos.</span><span class="sxs-lookup"><span data-stu-id="c88bd-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c88bd-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="c88bd-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="c88bd-115">duas</span><span class="sxs-lookup"><span data-stu-id="c88bd-115">2</span></span></p></td>
<td><p><span data-ttu-id="c88bd-116">Indica que o método <a href="addnew-method-ado.md">AddNew</a> foi chamado e o registro atual no buffer de cópias é um novo registro que não foi salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c88bd-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88bd-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="c88bd-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="c88bd-118">quatro</span><span class="sxs-lookup"><span data-stu-id="c88bd-118">4</span></span></p></td>
<td><p><span data-ttu-id="c88bd-119">Indica que o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="c88bd-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c88bd-120">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="c88bd-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="c88bd-121">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c88bd-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c88bd-122">Constant</span><span class="sxs-lookup"><span data-stu-id="c88bd-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c88bd-123">AdoEnums. EditMode. NONE</span><span class="sxs-lookup"><span data-stu-id="c88bd-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88bd-124">AdoEnums. EditMode. inPROGRESS</span><span class="sxs-lookup"><span data-stu-id="c88bd-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c88bd-125">AdoEnums. EditMode. ADD</span><span class="sxs-lookup"><span data-stu-id="c88bd-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88bd-126">AdoEnums. EditMode. DELETE</span><span class="sxs-lookup"><span data-stu-id="c88bd-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

