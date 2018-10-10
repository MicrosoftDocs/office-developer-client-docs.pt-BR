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
ms.openlocfilehash: 82dddbb7c9e73d602b9217a46df085e55795c996
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462374"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="3fcad-102">Propriedade Field.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="3fcad-102">Field.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="3fcad-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fcad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3fcad-p101">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3fcad-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fcad-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fcad-106">Syntax</span></span>

<span data-ttu-id="3fcad-107">*expressão* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="3fcad-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="3fcad-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="3fcad-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fcad-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fcad-109">Remarks</span></span>

<span data-ttu-id="3fcad-110">O valor de retorno é uma constante ou um valor **Long** que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3fcad-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fcad-111">Constante</span><span class="sxs-lookup"><span data-stu-id="3fcad-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="3fcad-112">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="3fcad-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-114">Geral (inglês, francês, alemão, português, italiano e espanhol moderno)</span><span class="sxs-lookup"><span data-stu-id="3fcad-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="3fcad-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-118">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="3fcad-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-120">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="3fcad-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-122">Russo</span><span class="sxs-lookup"><span data-stu-id="3fcad-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-124">Tcheco</span><span class="sxs-lookup"><span data-stu-id="3fcad-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-126">Holandês</span><span class="sxs-lookup"><span data-stu-id="3fcad-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-128">Grego</span><span class="sxs-lookup"><span data-stu-id="3fcad-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-130">Hebraico</span><span class="sxs-lookup"><span data-stu-id="3fcad-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="3fcad-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-134">Islandês</span><span class="sxs-lookup"><span data-stu-id="3fcad-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-136">Japonês</span><span class="sxs-lookup"><span data-stu-id="3fcad-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="3fcad-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-140">Neutro</span><span class="sxs-lookup"><span data-stu-id="3fcad-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-142">Norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="3fcad-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="3fcad-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-146">Paradox em norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="3fcad-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-148">Paradox em sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="3fcad-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-150">Polonês</span><span class="sxs-lookup"><span data-stu-id="3fcad-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="3fcad-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-154">Espanhol</span><span class="sxs-lookup"><span data-stu-id="3fcad-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-156">Sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="3fcad-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-158">Tailandês</span><span class="sxs-lookup"><span data-stu-id="3fcad-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-160">Turco</span><span class="sxs-lookup"><span data-stu-id="3fcad-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcad-162">Indefinido ou desconhecido</span><span class="sxs-lookup"><span data-stu-id="3fcad-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fcad-163">A disponibilidade da propriedade **CollatingOrder** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3fcad-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fcad-164">Se a coleção Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="3fcad-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="3fcad-165">CollatingOrder será</span><span class="sxs-lookup"><span data-stu-id="3fcad-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-166">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3fcad-167">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="3fcad-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-168">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3fcad-169">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3fcad-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-170">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3fcad-171">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3fcad-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcad-172">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3fcad-173">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="3fcad-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcad-174">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="3fcad-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3fcad-175">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3fcad-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fcad-176">A configuração da propriedade **CollatingOrder** corresponde ao argumento locale do método **CreateDatabase** quando o banco de dados foi criado ou o método **CompactDatabase** quando o banco de dados foi recentemente compactado.</span><span class="sxs-lookup"><span data-stu-id="3fcad-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="3fcad-p102">As definições das propriedades **CollatingOrder** e **Attributes** de um objeto **Field** em uma coleção **Fields** de um objeto **Index** determinam em conjunto a sequência e a direção da ordem de classificação de um índice. No entanto, não é possível definir uma ordem de agrupamento para um índice individual você pode defini-la somente para uma tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="3fcad-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

