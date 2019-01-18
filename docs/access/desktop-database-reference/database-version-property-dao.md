---
title: Propriedade Database.Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700064"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="44de7-102">Propriedade Database.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="44de7-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="44de7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="44de7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44de7-p101">Em um espaço de trabalho do Microsoft Access , retorna a versão do mecanismo de banco de dados do Microsoft Jet ou do Microsoft Access que criou o banco de dados. **String** de somente leitura.</span><span class="sxs-lookup"><span data-stu-id="44de7-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="44de7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44de7-106">Syntax</span></span>

<span data-ttu-id="44de7-107">*expressão* . Versão</span><span class="sxs-lookup"><span data-stu-id="44de7-107">*expression* .Version</span></span>

<span data-ttu-id="44de7-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="44de7-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44de7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="44de7-109">Remarks</span></span>

<span data-ttu-id="44de7-110">O valor de retorno é uma cadeia de caracteres que avalia o número da versão, formatado como se segue.</span><span class="sxs-lookup"><span data-stu-id="44de7-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="44de7-p102">O espaço de trabalho do Microsoft Access representa o número da versão na fórmula "*maior.menor*". Por exemplo, "3.0". O número da versão do produto é composto do número da versão (3), de um ponto e do número do lançamento (0).</span><span class="sxs-lookup"><span data-stu-id="44de7-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="44de7-114">A tabela a seguir mostra qual versão do mecanismo do banco de dados foi incluída nas várias versões dos produtos Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44de7-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44de7-115">Mecanismo do Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="44de7-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="44de7-116">Versão (ano do lançamento)</span><span class="sxs-lookup"><span data-stu-id="44de7-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="44de7-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="44de7-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="44de7-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="44de7-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="44de7-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="44de7-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="44de7-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="44de7-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44de7-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="44de7-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="44de7-123">1.0</span><span class="sxs-lookup"><span data-stu-id="44de7-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="44de7-124">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-125">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-126">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44de7-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="44de7-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="44de7-129">1.1</span><span class="sxs-lookup"><span data-stu-id="44de7-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="44de7-130">3.0</span><span class="sxs-lookup"><span data-stu-id="44de7-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="44de7-131">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-132">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44de7-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="44de7-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="44de7-135">2.0</span><span class="sxs-lookup"><span data-stu-id="44de7-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="44de7-136">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-137">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-138">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44de7-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="44de7-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="44de7-141">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-142">4.0 (16 bits)</span><span class="sxs-lookup"><span data-stu-id="44de7-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="44de7-143">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="44de7-144">N/D</span><span class="sxs-lookup"><span data-stu-id="44de7-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44de7-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="44de7-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="44de7-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="44de7-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="44de7-148">4.0 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="44de7-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="44de7-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="44de7-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="44de7-150">4. x</span><span class="sxs-lookup"><span data-stu-id="44de7-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44de7-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="44de7-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="44de7-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="44de7-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="44de7-154">5.0</span><span class="sxs-lookup"><span data-stu-id="44de7-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="44de7-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="44de7-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="44de7-156">5.0</span><span class="sxs-lookup"><span data-stu-id="44de7-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44de7-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="44de7-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="44de7-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="44de7-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="44de7-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="44de7-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="44de7-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="44de7-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44de7-161">Mecanismo do banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="44de7-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="44de7-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="44de7-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="44de7-163">2007</span><span class="sxs-lookup"><span data-stu-id="44de7-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

