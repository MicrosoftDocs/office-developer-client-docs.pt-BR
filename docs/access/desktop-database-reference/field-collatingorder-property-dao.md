---
title: Propriedade Field.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d64620ccf1c0d011c060ac829223041f49bde9d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925286"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="1ab73-102">Propriedade Field.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ab73-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="1ab73-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ab73-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ab73-p101">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1ab73-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab73-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ab73-106">Syntax</span></span>

<span data-ttu-id="1ab73-107">*expressão* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="1ab73-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="1ab73-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="1ab73-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ab73-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ab73-109">Remarks</span></span>

<span data-ttu-id="1ab73-110">O valor de retorno é uma constante ou um valor **Long** que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ab73-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ab73-111">Constante</span><span class="sxs-lookup"><span data-stu-id="1ab73-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="1ab73-112">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="1ab73-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-114">Geral (inglês, francês, alemão, português, italiano e espanhol moderno)</span><span class="sxs-lookup"><span data-stu-id="1ab73-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="1ab73-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-118">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="1ab73-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-120">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="1ab73-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-122">Russo</span><span class="sxs-lookup"><span data-stu-id="1ab73-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-124">Tcheco</span><span class="sxs-lookup"><span data-stu-id="1ab73-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-126">Holandês</span><span class="sxs-lookup"><span data-stu-id="1ab73-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-128">Grego</span><span class="sxs-lookup"><span data-stu-id="1ab73-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-130">Hebraico</span><span class="sxs-lookup"><span data-stu-id="1ab73-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="1ab73-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-134">Islandês</span><span class="sxs-lookup"><span data-stu-id="1ab73-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-136">Japonês</span><span class="sxs-lookup"><span data-stu-id="1ab73-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="1ab73-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-140">Neutro</span><span class="sxs-lookup"><span data-stu-id="1ab73-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-142">Norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="1ab73-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="1ab73-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-146">Paradox em norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="1ab73-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-148">Paradox em sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="1ab73-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-150">Polonês</span><span class="sxs-lookup"><span data-stu-id="1ab73-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="1ab73-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-154">Espanhol</span><span class="sxs-lookup"><span data-stu-id="1ab73-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-156">Sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="1ab73-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-158">Tailandês</span><span class="sxs-lookup"><span data-stu-id="1ab73-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-160">Turco</span><span class="sxs-lookup"><span data-stu-id="1ab73-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="1ab73-162">Indefinido ou desconhecido</span><span class="sxs-lookup"><span data-stu-id="1ab73-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ab73-163">A disponibilidade da propriedade **CollatingOrder** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ab73-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ab73-164">Se a coleção Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="1ab73-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="1ab73-165">CollatingOrder será</span><span class="sxs-lookup"><span data-stu-id="1ab73-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-166">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1ab73-167">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="1ab73-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-168">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1ab73-169">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab73-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-170">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1ab73-171">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab73-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ab73-172">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1ab73-173">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="1ab73-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ab73-174">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="1ab73-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1ab73-175">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab73-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ab73-176">A configuração da propriedade **CollatingOrder** corresponde ao argumento locale do método **CreateDatabase** quando o banco de dados foi criado ou o método **CompactDatabase** quando o banco de dados foi recentemente compactado.</span><span class="sxs-lookup"><span data-stu-id="1ab73-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="1ab73-p102">As definições das propriedades **CollatingOrder** e **Attributes** de um objeto **Field** em uma coleção **Fields** de um objeto **Index** determinam em conjunto a sequência e a direção da ordem de classificação de um índice. No entanto, não é possível definir uma ordem de agrupamento para um índice individual você pode defini-la somente para uma tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="1ab73-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

