---
title: Propriedade Field2.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 508f7f758d682dec0f1557f8a3f4dc2845e20a39
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870764"
---
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="4c210-102">Propriedade Field2.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="4c210-102">Field2.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="4c210-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c210-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c210-p101">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4c210-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c210-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c210-106">Syntax</span></span>

<span data-ttu-id="4c210-107">*expressão* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="4c210-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="4c210-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="4c210-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c210-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c210-109">Remarks</span></span>

<span data-ttu-id="4c210-110">O valor de retorno é uma constante ou um valor **Long** que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c210-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c210-111">Constante</span><span class="sxs-lookup"><span data-stu-id="4c210-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="4c210-112">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="4c210-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c210-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-114">Geral (inglês, francês, alemão, português, italiano e espanhol moderno)</span><span class="sxs-lookup"><span data-stu-id="4c210-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="4c210-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-118">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="4c210-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-120">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="4c210-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-122">Russo</span><span class="sxs-lookup"><span data-stu-id="4c210-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-124">Tcheco</span><span class="sxs-lookup"><span data-stu-id="4c210-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-126">Holandês</span><span class="sxs-lookup"><span data-stu-id="4c210-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-128">Grego</span><span class="sxs-lookup"><span data-stu-id="4c210-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-130">Hebraico</span><span class="sxs-lookup"><span data-stu-id="4c210-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="4c210-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-134">Islandês</span><span class="sxs-lookup"><span data-stu-id="4c210-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-136">Japonês</span><span class="sxs-lookup"><span data-stu-id="4c210-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="4c210-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-140">Neutro</span><span class="sxs-lookup"><span data-stu-id="4c210-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-142">Norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="4c210-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="4c210-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-146">Paradox em norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="4c210-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-148">Paradox em sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="4c210-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-150">Polonês</span><span class="sxs-lookup"><span data-stu-id="4c210-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="4c210-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-154">Espanhol</span><span class="sxs-lookup"><span data-stu-id="4c210-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-156">Sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="4c210-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-158">Tailandês</span><span class="sxs-lookup"><span data-stu-id="4c210-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-160">Turco</span><span class="sxs-lookup"><span data-stu-id="4c210-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="4c210-162">Indefinido ou desconhecido</span><span class="sxs-lookup"><span data-stu-id="4c210-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c210-163">A disponibilidade da propriedade **CollatingOrder** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c210-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c210-164">Se a coleção Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="4c210-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="4c210-165">CollatingOrder será</span><span class="sxs-lookup"><span data-stu-id="4c210-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c210-166">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4c210-167">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4c210-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-168">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4c210-169">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c210-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-170">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4c210-171">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c210-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c210-172">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4c210-173">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4c210-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c210-174">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4c210-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4c210-175">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c210-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c210-176">A configuração da propriedade **CollatingOrder** corresponde ao argumento locale do método **CreateDatabase** quando o banco de dados foi criado ou o método **CompactDatabase** quando o banco de dados foi recentemente compactado.</span><span class="sxs-lookup"><span data-stu-id="4c210-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="4c210-p102">As configurações das propriedades **CollatingOrder** e **Attributes** de um objeto **Field2** em uma coleção **Fields** de um objeto **Index** determinam a sequência e a direção da ordem de classificação em um índice. Entretanto, você não pode definir uma ordem de agrupamento para um índice individual  você pode defini-la apenas para uma tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="4c210-p102">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

