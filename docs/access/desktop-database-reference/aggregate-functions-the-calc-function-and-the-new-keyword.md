---
title: Funções de agregação, a função CALC e a palavra-chave NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb3e667a23d5bfd1d3dda5b4eb8dbd60a47e36ba
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025984"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="1be68-102">Funções de agregação, a função CALC e a palavra-chave NEW</span><span class="sxs-lookup"><span data-stu-id="1be68-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="1be68-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1be68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1be68-p101">A técnica data shaping oferece suporte para as funções a seguir. O nome atribuído ao capítulo que contém a coluna a ser operada é o *chapter-alias*.</span><span class="sxs-lookup"><span data-stu-id="1be68-p101">Data shaping supports the following functions. The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="1be68-106">Um alias de capítulo pode ser totalmente qualificado, consistindo em cada nome de coluna de capítulo levando o capítulo contendo o *nome da coluna,* todos separados por pontos.</span><span class="sxs-lookup"><span data-stu-id="1be68-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="1be68-107">Por exemplo, se o capítulo pai, chap1, contiver um capítulo filho, chap2, que tenha uma coluna de quantidade, amt, então o nome qualificado será chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="1be68-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be68-108">Funções agregadas</span><span class="sxs-lookup"><span data-stu-id="1be68-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="1be68-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1be68-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be68-110">Soma (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-111">Calcula a soma de todos os valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="1be68-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-112">AVG (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-113">Calcula a média de todos os valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="1be68-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-114">MAX (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-115">Calcula o valor máximo na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="1be68-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-116">MIN (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-117">Calcula o valor mínimo na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="1be68-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-118">COUNT (<em>capítulo-alias</em>[.<em> nome da coluna</em>])</span><span class="sxs-lookup"><span data-stu-id="1be68-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="1be68-p103">Conta o número de linhas no alias especificado. Se uma coluna for especificada, somente as linhas para as quais essa coluna for não-Null serão incluídas na contagem.</span><span class="sxs-lookup"><span data-stu-id="1be68-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-121">DESVPAD (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-122">Calcula o desvio padrão na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="1be68-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-123">QUALQUER (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-p104">Um valor da coluna especificada. ANY possui um valor previsível apenas quando o valor da coluna é igual para todas as linhas do capítulo.
</span><span class="sxs-lookup"><span data-stu-id="1be68-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="1be68-126"><strong>Observação</strong>: se a coluna não contiver o mesmo valor para todas as linhas no capítulo, o comando de forma arbitrariamente retorna um dos valores como o valor da qualquer função.</span><span class="sxs-lookup"><span data-stu-id="1be68-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
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
<th><p><span data-ttu-id="1be68-127">Expressão calculada</span><span class="sxs-lookup"><span data-stu-id="1be68-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="1be68-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="1be68-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be68-129">CALC(<em>expression</em>)</span><span class="sxs-lookup"><span data-stu-id="1be68-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="1be68-p105">Calcula uma expressão arbitrária, mas apenas na linha do <strong>Recordset</strong> que contém a função CALC. Qualquer expressão que usar essas <a href="visual-basic-for-applications-functions.md">Funções do Visual Basic for Applications (VBA)</a> é permitida.</span><span class="sxs-lookup"><span data-stu-id="1be68-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
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
<th><p><span data-ttu-id="1be68-132">Palavra-chave NEW</span><span class="sxs-lookup"><span data-stu-id="1be68-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="1be68-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="1be68-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be68-134">NOVO <em>tipo de campo</em> [(<em>largura</em> | <em>escala</em> | <em>precisão</em> | <em>erro</em> [, <em>escala</em> | <em>erro</em>])]</span><span class="sxs-lookup"><span data-stu-id="1be68-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="1be68-135">Adiciona ao <strong>Recordset</strong> uma coluna vazia do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="1be68-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1be68-136">O *field-type* passado com a palavra-chave NEW pode ser qualquer um dos tipos de dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="1be68-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be68-137">Tipos de dados do OLE DB</span><span class="sxs-lookup"><span data-stu-id="1be68-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="1be68-138">Equivalente(s) ao tipo de dados do ADO</span><span class="sxs-lookup"><span data-stu-id="1be68-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be68-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="1be68-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="1be68-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="1be68-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="1be68-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="1be68-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="1be68-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="1be68-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="1be68-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="1be68-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-145">DBTYPE_U1</span><span class="sxs-lookup"><span data-stu-id="1be68-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="1be68-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="1be68-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="1be68-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="1be68-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="1be68-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-149">DBTYPE_U2</span><span class="sxs-lookup"><span data-stu-id="1be68-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="1be68-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="1be68-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-151">DBTYPE_U4</span><span class="sxs-lookup"><span data-stu-id="1be68-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="1be68-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="1be68-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="1be68-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="1be68-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="1be68-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-155">DBTYPE_U8</span><span class="sxs-lookup"><span data-stu-id="1be68-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="1be68-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="1be68-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="1be68-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="1be68-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="1be68-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="1be68-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="1be68-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="1be68-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="1be68-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="1be68-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="1be68-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="1be68-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="1be68-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="1be68-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="1be68-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="1be68-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="1be68-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="1be68-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="1be68-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="1be68-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="1be68-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="1be68-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="1be68-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="1be68-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="1be68-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="1be68-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="1be68-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="1be68-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="1be68-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be68-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="1be68-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="1be68-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="1be68-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be68-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="1be68-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="1be68-178">adError</span><span class="sxs-lookup"><span data-stu-id="1be68-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1be68-179">Quando o novo campo é do tipo decimal (no OLE DB, DBTYPE\_DECIMAL, ou no ADO, adDecimal), você deve especificar os valores de precisão e escala.</span><span class="sxs-lookup"><span data-stu-id="1be68-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

