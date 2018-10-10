---
title: EditModeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7322193971e4230afaacbb1f614c7ab682f3c149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463879"
---
# <a name="editmodeenum"></a><span data-ttu-id="19b20-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="19b20-102">EditModeEnum</span></span>


<span data-ttu-id="19b20-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19b20-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19b20-104">Especifica o status de edição de um registro.</span><span class="sxs-lookup"><span data-stu-id="19b20-104">Specifies the editing status of a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19b20-105">Constante</span><span class="sxs-lookup"><span data-stu-id="19b20-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="19b20-106">Valor</span><span class="sxs-lookup"><span data-stu-id="19b20-106">Value</span></span></p></th>
<th><p><span data-ttu-id="19b20-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="19b20-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19b20-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="19b20-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="19b20-109">0</span><span class="sxs-lookup"><span data-stu-id="19b20-109">0</span></span></p></td>
<td><p><span data-ttu-id="19b20-110">Indica que nenhuma operação de edição está em andamento.</span><span class="sxs-lookup"><span data-stu-id="19b20-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b20-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="19b20-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="19b20-112">1</span><span class="sxs-lookup"><span data-stu-id="19b20-112">1</span></span></p></td>
<td><p><span data-ttu-id="19b20-113">Indica que os dados no registro atual foram modificados, mas não foram salvos.</span><span class="sxs-lookup"><span data-stu-id="19b20-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b20-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="19b20-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="19b20-115">2</span><span class="sxs-lookup"><span data-stu-id="19b20-115">2</span></span></p></td>
<td><p><span data-ttu-id="19b20-116">Indica que o método <a href="addnew-method-ado.md">AddNew</a> foi chamado e o registro atual no buffer de cópias é um novo registro que não foi salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="19b20-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b20-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="19b20-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="19b20-118">4</span><span class="sxs-lookup"><span data-stu-id="19b20-118">4</span></span></p></td>
<td><p><span data-ttu-id="19b20-119">Indica que o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="19b20-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19b20-120">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="19b20-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="19b20-121">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="19b20-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19b20-122">Constante</span><span class="sxs-lookup"><span data-stu-id="19b20-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19b20-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="19b20-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b20-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="19b20-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b20-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="19b20-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b20-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="19b20-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

