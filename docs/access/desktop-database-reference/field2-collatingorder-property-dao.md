---
title: Propriedade Campo2. CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02711fbbf39b058bb88e9568716169825ae4a923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292864"
---
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="5bd5b-102">Propriedade Campo2. CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="5bd5b-102">Field2.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="5bd5b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bd5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bd5b-p101">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5bd5b-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd5b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bd5b-106">Syntax</span></span>

<span data-ttu-id="5bd5b-107">*expressão* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="5bd5b-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="5bd5b-108">*expressão* Uma variável que representa um objeto **campo2** .</span><span class="sxs-lookup"><span data-stu-id="5bd5b-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd5b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bd5b-109">Remarks</span></span>

<span data-ttu-id="5bd5b-110">O valor de retorno é uma constante ou um valor **Long** que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bd5b-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bd5b-111">Constant</span><span class="sxs-lookup"><span data-stu-id="5bd5b-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="5bd5b-112">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="5bd5b-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-114">Geral (inglês, francês, alemão, português, italiano e espanhol moderno)</span><span class="sxs-lookup"><span data-stu-id="5bd5b-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="5bd5b-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-118">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="5bd5b-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-120">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="5bd5b-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-122">Russo</span><span class="sxs-lookup"><span data-stu-id="5bd5b-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-124">Tcheco</span><span class="sxs-lookup"><span data-stu-id="5bd5b-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-126">Holandês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-128">Grego</span><span class="sxs-lookup"><span data-stu-id="5bd5b-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-130">Hebraico</span><span class="sxs-lookup"><span data-stu-id="5bd5b-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="5bd5b-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-134">Islandês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-136">Japonês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="5bd5b-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-140">Neutro</span><span class="sxs-lookup"><span data-stu-id="5bd5b-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-142">Norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-144">International Paradox</span><span class="sxs-lookup"><span data-stu-id="5bd5b-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-146">Norueguês ou dinamarquês Paradox</span><span class="sxs-lookup"><span data-stu-id="5bd5b-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-148">Sueco ou finlandês Paradox</span><span class="sxs-lookup"><span data-stu-id="5bd5b-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-150">Polonês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="5bd5b-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-154">Espanhol</span><span class="sxs-lookup"><span data-stu-id="5bd5b-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-156">Sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-158">Tailandês</span><span class="sxs-lookup"><span data-stu-id="5bd5b-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-160">Turco</span><span class="sxs-lookup"><span data-stu-id="5bd5b-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd5b-162">Indefinido ou desconhecido</span><span class="sxs-lookup"><span data-stu-id="5bd5b-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5bd5b-163">A disponibilidade da propriedade **CollatingOrder** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bd5b-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bd5b-164">Se a coleção Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="5bd5b-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="5bd5b-165">Então CollatingOrder é</span><span class="sxs-lookup"><span data-stu-id="5bd5b-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-166">
						Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5bd5b-167">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="5bd5b-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-168">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5bd5b-169">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bd5b-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-170">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5bd5b-171">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bd5b-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd5b-172">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5bd5b-173">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="5bd5b-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd5b-174">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="5bd5b-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5bd5b-175">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bd5b-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5bd5b-176">A configuração da propriedade **CollatingOrder** corresponde ao argumento locale do método **CreateDatabase** quando o banco de dados foi criado ou o método **CompactDatabase** quando o banco de dados foi compactado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="5bd5b-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="5bd5b-p102">As configurações das propriedades **CollatingOrder** e **Attributes** de um objeto **Field2** em uma coleção **Fields** de um objeto **Index** determinam a sequência e a direção da ordem de classificação em um índice. Entretanto, você não pode definir uma ordem de agrupamento para um índice individual  você pode defini-la apenas para uma tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="5bd5b-p102">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

