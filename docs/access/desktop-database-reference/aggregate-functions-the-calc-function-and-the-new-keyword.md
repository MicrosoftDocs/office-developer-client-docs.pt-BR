---
title: Funções de agregação, a função CALC e a palavra-chave NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297190"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="dbf88-102">Funções de agregação, a função CALC e a palavra-chave NEW</span><span class="sxs-lookup"><span data-stu-id="dbf88-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="dbf88-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbf88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbf88-104">A técnica data shaping oferece suporte para as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="dbf88-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="dbf88-105">O nome atribuído ao capítulo que contém a coluna a ser operada é o *chapter-alias*.</span><span class="sxs-lookup"><span data-stu-id="dbf88-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="dbf88-p102">Um chapter-alias pode ser totalmente qualificado, consistindo no nome de coluna de cada capítulo, levando ao capítulo que contém o *column-name*, todos separados por pontos. Por exemplo, se o capítulo pai, chap1, contiver um capítulo filho, chap2, que tenha uma coluna de quantidade, amt, então o nome qualificado será chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="dbf88-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbf88-108">Funções agregadas</span><span class="sxs-lookup"><span data-stu-id="dbf88-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="dbf88-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbf88-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-110">SUM (<em>Chapter-alias</em>.<em> Column-Name</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-111">Calcula a soma de todos os valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="dbf88-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-112">Méd (<em>Chapter-alias</em>.<em> Column-Name</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-113">Calcula a média de todos os valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="dbf88-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-114">MAX (<em>Chapter-alias</em>.<em> Column-Name</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-115">Calcula o valor máximo na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="dbf88-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-116">MIN (<em>Chapter-alias</em>.<em> Column-Name</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-117">Calcula o valor mínimo na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="dbf88-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-118">COUNT (<em>Chapter-alias</em>[.<em> Column-Name</em>])</span><span class="sxs-lookup"><span data-stu-id="dbf88-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="dbf88-p103">Conta o número de linhas no alias especificado. Se uma coluna for especificada, somente as linhas para as quais essa coluna for não-Null serão incluídas na contagem.</span><span class="sxs-lookup"><span data-stu-id="dbf88-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-121">DESVPAD (<em>Chapter-alias</em>.<em> Column-Name</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-122">Calcula o desvio padrão na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="dbf88-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-123">QUALQUER (<em>Chapter-alias</em>.<em> Column-Name</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-124">Um valor da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="dbf88-124">A value of the specified column.</span></span> <span data-ttu-id="dbf88-125">ANY possui um valor previsível apenas quando o valor da coluna é igual para todas as linhas do capítulo.</span><span class="sxs-lookup"><span data-stu-id="dbf88-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="dbf88-126"><strong>Observação</strong>: se a coluna não contiver o mesmo valor para todas as linhas no capítulo, o comando Shape retorna arbitrariamente um dos valores para ser o valor da função qualquer.</span><span class="sxs-lookup"><span data-stu-id="dbf88-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbf88-127">Expressão calculada</span><span class="sxs-lookup"><span data-stu-id="dbf88-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="dbf88-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbf88-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-129">CALC (<em>expressão</em>)</span><span class="sxs-lookup"><span data-stu-id="dbf88-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="dbf88-p105">Calcula uma expressão arbitrária, mas apenas na linha do <strong>Recordset</strong> que contém a função CALC. Qualquer expressão que usar essas <a href="visual-basic-for-applications-functions.md">Funções do Visual Basic for Applications (VBA)</a> é permitida.</span><span class="sxs-lookup"><span data-stu-id="dbf88-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbf88-132">Palavra-chave NEW</span><span class="sxs-lookup"><span data-stu-id="dbf88-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="dbf88-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbf88-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-134">Novo <em>campo-tipo</em> [(<em>erro</em> de<em>precisão</em> | de<em>escala</em> | de<em>largura</em> | [, <em>escala</em> | de<em>erro</em>])]</span><span class="sxs-lookup"><span data-stu-id="dbf88-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="dbf88-135">Adiciona ao <strong>Recordset</strong> uma coluna vazia do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="dbf88-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="dbf88-136">O *field-type* passado com a palavra-chave NEW pode ser qualquer um dos tipos de dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="dbf88-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbf88-137">Tipos de dados do OLE DB</span><span class="sxs-lookup"><span data-stu-id="dbf88-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="dbf88-138">Equivalente(s) ao tipo de dados do ADO</span><span class="sxs-lookup"><span data-stu-id="dbf88-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="dbf88-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="dbf88-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="dbf88-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="dbf88-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="dbf88-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="dbf88-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="dbf88-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="dbf88-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="dbf88-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="dbf88-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="dbf88-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="dbf88-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="dbf88-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="dbf88-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="dbf88-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="dbf88-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="dbf88-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="dbf88-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="dbf88-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="dbf88-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="dbf88-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="dbf88-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="dbf88-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="dbf88-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="dbf88-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="dbf88-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="dbf88-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dbf88-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="dbf88-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="dbf88-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="dbf88-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="dbf88-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="dbf88-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="dbf88-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="dbf88-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="dbf88-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="dbf88-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="dbf88-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="dbf88-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="dbf88-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="dbf88-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="dbf88-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="dbf88-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="dbf88-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="dbf88-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="dbf88-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="dbf88-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="dbf88-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="dbf88-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="dbf88-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="dbf88-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="dbf88-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="dbf88-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="dbf88-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf88-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="dbf88-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="dbf88-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="dbf88-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf88-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="dbf88-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="dbf88-178">adError</span><span class="sxs-lookup"><span data-stu-id="dbf88-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dbf88-179">Quando o novo campo é do tipo decimal (no OLE DB, no\_formato DB decimal ou no ADO, adDecimal), você deve especificar os valores de precisão e escala.</span><span class="sxs-lookup"><span data-stu-id="dbf88-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

