---
title: AffectEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297197"
---
# <a name="affectenum"></a><span data-ttu-id="a1cfd-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="a1cfd-102">AffectEnum</span></span>

<span data-ttu-id="a1cfd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1cfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1cfd-104">Especifica quais registros foram afetados por uma operação.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1cfd-105">Constant</span><span class="sxs-lookup"><span data-stu-id="a1cfd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a1cfd-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a1cfd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a1cfd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1cfd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1cfd-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="a1cfd-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="a1cfd-109">3D</span><span class="sxs-lookup"><span data-stu-id="a1cfd-109">3</span></span></p></td>
<td><p><span data-ttu-id="a1cfd-110">Se não houver um <a href="filter-property-ado.md">Filter</a> aplicado ao <strong>Recordset</strong>, afeta todos os registros.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="a1cfd-111">Se a propriedade <strong>Filter</strong> estiver definida como um critério de cadeia de caracteres &quot;(como autor = '&quot;Smith '), a operação afetará os registros visíveis no capítulo atual.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="a1cfd-112">Se a propriedade <strong>Filter</strong> estiver definida como um membro do <a href="filtergroupenum.md">FilterGroupEnum</a> ou uma matriz de indicadores, a operação afetará todas as linhas do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="a1cfd-113"><strong>Observação</strong>: o adAffectAll está oculto no navegador de objetos do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1cfd-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="a1cfd-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="a1cfd-115">quatro</span><span class="sxs-lookup"><span data-stu-id="a1cfd-115">4</span></span></p></td>
<td><p><span data-ttu-id="a1cfd-116">Afeta todos os registros em todos os capítulos irmãos do <strong>Recordset</strong>, incluindo os que não são visíveis através de qualquer <strong>Filter</strong> que esteja aplicado no momento.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1cfd-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="a1cfd-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="a1cfd-118">1</span><span class="sxs-lookup"><span data-stu-id="a1cfd-118">1</span></span></p></td>
<td><p><span data-ttu-id="a1cfd-119">Afeta apenas o registro atual.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1cfd-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="a1cfd-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="a1cfd-121">duas</span><span class="sxs-lookup"><span data-stu-id="a1cfd-121">2</span></span></p></td>
<td><p><span data-ttu-id="a1cfd-p102">Afeta apenas os registros que satisfazem a definição da propriedade <a href="filter-property-ado.md">Filter</a> atual. Você deve definir a propriedade <strong>Filter</strong> para um valor <strong>FilterGroupEnum</strong> ou uma matriz de <strong>Indicadores</strong> para utilizar essa opção.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a1cfd-124">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a1cfd-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="a1cfd-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a1cfd-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1cfd-126">Constant</span><span class="sxs-lookup"><span data-stu-id="a1cfd-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1cfd-127">AdoEnums. afeto. ALL</span><span class="sxs-lookup"><span data-stu-id="a1cfd-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1cfd-128">AdoEnums..</span><span class="sxs-lookup"><span data-stu-id="a1cfd-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1cfd-129">AdoEnums. afeto. CURRENT</span><span class="sxs-lookup"><span data-stu-id="a1cfd-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1cfd-130">AdoEnums. afeto. GROUP</span><span class="sxs-lookup"><span data-stu-id="a1cfd-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

