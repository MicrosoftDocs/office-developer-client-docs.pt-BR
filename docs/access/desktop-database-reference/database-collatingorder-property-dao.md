---
title: Propriedade Database.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21d775c0abac5d2afddd6b0930816c8d6d381ff0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700889"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="750ff-102">Propriedade Database.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="750ff-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="750ff-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="750ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="750ff-p101">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="750ff-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="750ff-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="750ff-106">Syntax</span></span>

<span data-ttu-id="750ff-107">*expressão* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="750ff-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="750ff-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="750ff-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="750ff-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="750ff-109">Remarks</span></span>

<span data-ttu-id="750ff-110">O valor de retorno é uma constante ou um valor **Long** que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="750ff-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750ff-111">Constante</span><span class="sxs-lookup"><span data-stu-id="750ff-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="750ff-112">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="750ff-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750ff-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-114">Geral (inglês, francês, alemão, português, italiano e espanhol moderno)</span><span class="sxs-lookup"><span data-stu-id="750ff-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="750ff-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-118">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="750ff-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-120">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="750ff-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-122">Russo</span><span class="sxs-lookup"><span data-stu-id="750ff-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-124">Tcheco</span><span class="sxs-lookup"><span data-stu-id="750ff-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-126">Holandês</span><span class="sxs-lookup"><span data-stu-id="750ff-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-128">Grego</span><span class="sxs-lookup"><span data-stu-id="750ff-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-130">Hebraico</span><span class="sxs-lookup"><span data-stu-id="750ff-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="750ff-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-134">Islandês</span><span class="sxs-lookup"><span data-stu-id="750ff-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-136">Japonês</span><span class="sxs-lookup"><span data-stu-id="750ff-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="750ff-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-140">Neutro</span><span class="sxs-lookup"><span data-stu-id="750ff-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-142">Norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="750ff-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="750ff-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-146">Paradox em norueguês ou dinamarquês</span><span class="sxs-lookup"><span data-stu-id="750ff-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-148">Paradox em sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="750ff-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-150">Polonês</span><span class="sxs-lookup"><span data-stu-id="750ff-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="750ff-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-154">Espanhol</span><span class="sxs-lookup"><span data-stu-id="750ff-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-156">Sueco ou finlandês</span><span class="sxs-lookup"><span data-stu-id="750ff-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-158">Tailandês</span><span class="sxs-lookup"><span data-stu-id="750ff-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750ff-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-160">Turco</span><span class="sxs-lookup"><span data-stu-id="750ff-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750ff-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="750ff-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="750ff-162">Indefinido ou desconhecido</span><span class="sxs-lookup"><span data-stu-id="750ff-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="750ff-163">A configuração da propriedade **CollatingOrder** corresponde ao argumento locale do método **CreateDatabase** quando o banco de dados foi criado ou o método **CompactDatabase** quando o banco de dados foi recentemente compactado.</span><span class="sxs-lookup"><span data-stu-id="750ff-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="750ff-p102">Verifique a configuração da propriedade **CollatingOrder** de um objeto **Database** ou **Field** para determinar o método de comparação da sequência para o banco de dados ou o campo. Você pode definir a propriedade **CollatingOrder** de um objeto **Field** novo e não acrescentado se quiser que a configuração do objeto **Field** seja diferente da configuração do objeto **Database** que a contém.</span><span class="sxs-lookup"><span data-stu-id="750ff-p102">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field. You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

