---
title: AffectEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9725a0e4af6ac6d25140739d6604abae6b76dcb6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879442"
---
# <a name="affectenum"></a><span data-ttu-id="ebdba-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="ebdba-102">AffectEnum</span></span>

<span data-ttu-id="ebdba-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebdba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebdba-104">Especifica quais registros foram afetados por uma operação.</span><span class="sxs-lookup"><span data-stu-id="ebdba-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebdba-105">Constante</span><span class="sxs-lookup"><span data-stu-id="ebdba-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ebdba-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ebdba-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ebdba-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebdba-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebdba-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="ebdba-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdba-109">3</span><span class="sxs-lookup"><span data-stu-id="ebdba-109">3</span></span></p></td>
<td><p><span data-ttu-id="ebdba-110">Se não houver um <a href="filter-property-ado.md">Filter</a> aplicado ao <strong>Recordset</strong>, afeta todos os registros.
</span><span class="sxs-lookup"><span data-stu-id="ebdba-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="ebdba-111">Se a propriedade <strong>Filter</strong> estiver definida como um critério de sequência (como &quot;Author = 'Smith'&quot;), a operação afetará os registros visíveis no capítulo atual.</span><span class="sxs-lookup"><span data-stu-id="ebdba-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="ebdba-112">Se a propriedade <strong>Filter</strong> estiver definida como membro do <a href="filtergroupenum.md">FilterGroupEnum</a> ou uma matriz de indicadores, a operação afetará todas as linhas do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebdba-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>
<p><span data-ttu-id="ebdba-113"><strong>Observação</strong>: adAffectAll está oculto no Visual Basic Object Browser.</span><span class="sxs-lookup"><span data-stu-id="ebdba-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdba-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="ebdba-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdba-115">4</span><span class="sxs-lookup"><span data-stu-id="ebdba-115">4</span></span></p></td>
<td><p><span data-ttu-id="ebdba-116">Afeta todos os registros em todos os capítulos irmãos do <strong>Recordset</strong>, incluindo os que não são visíveis através de qualquer <strong>Filter</strong> que esteja aplicado no momento.</span><span class="sxs-lookup"><span data-stu-id="ebdba-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdba-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="ebdba-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdba-118">1</span><span class="sxs-lookup"><span data-stu-id="ebdba-118">1</span></span></p></td>
<td><p><span data-ttu-id="ebdba-119">Afeta apenas o registro atual.</span><span class="sxs-lookup"><span data-stu-id="ebdba-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdba-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="ebdba-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdba-121">2</span><span class="sxs-lookup"><span data-stu-id="ebdba-121">2</span></span></p></td>
<td><p><span data-ttu-id="ebdba-p102">Afeta apenas os registros que satisfazem a definição da propriedade <a href="filter-property-ado.md">Filter</a> atual. Você deve definir a propriedade <strong>Filter</strong> para um valor <strong>FilterGroupEnum</strong> ou uma matriz de <strong>Indicadores</strong> para utilizar essa opção.</span><span class="sxs-lookup"><span data-stu-id="ebdba-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ebdba-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ebdba-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="ebdba-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ebdba-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebdba-126">Constante</span><span class="sxs-lookup"><span data-stu-id="ebdba-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebdba-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="ebdba-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdba-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="ebdba-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdba-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="ebdba-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdba-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="ebdba-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

