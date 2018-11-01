---
title: Funções agregadas, a função CALC e a palavra-chave NEW
TOCTitle: Aggregate Functions, the CALC Function, and the NEW Keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ee1bff23e1bcf04c1a9fd4cfc807edbd541148
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882375"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="d2166-102">Funções agregadas, a função CALC e a palavra-chave NEW</span><span class="sxs-lookup"><span data-stu-id="d2166-102">Aggregate Functions, the CALC Function, and the NEW Keyword</span></span>


<span data-ttu-id="d2166-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2166-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2166-p101">A técnica data shaping oferece suporte para as funções a seguir. O nome atribuído ao capítulo que contém a coluna a ser operada é o *chapter-alias*.</span><span class="sxs-lookup"><span data-stu-id="d2166-p101">Data shaping supports the following functions. The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="d2166-p102">Um chapter-alias pode ser totalmente qualificado, consistindo no nome de coluna de cada capítulo, levando ao capítulo que contém o *column-name*, todos separados por pontos. Por exemplo, se o capítulo pai, chap1, contiver um capítulo filho, chap2, que tenha uma coluna de quantidade, amt, então o nome qualificado será chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="d2166-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2166-108">Funções agregadas</span><span class="sxs-lookup"><span data-stu-id="d2166-108">Aggregate Functions</span></span></p></th>
<th><p><span data-ttu-id="d2166-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2166-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2166-110">Soma (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-111">Calcula a soma de todos os valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="d2166-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-112">AVG (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-113">Calcula a média de todos os valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="d2166-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-114">MAX (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-115">Calcula o valor máximo na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="d2166-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-116">MIN (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-117">Calcula o valor mínimo na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="d2166-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-118">COUNT (<em>capítulo-alias</em>[.<em> nome da coluna</em>])</span><span class="sxs-lookup"><span data-stu-id="d2166-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="d2166-p103">Conta o número de linhas no alias especificado. Se uma coluna for especificada, somente as linhas para as quais essa coluna for não-Null serão incluídas na contagem.</span><span class="sxs-lookup"><span data-stu-id="d2166-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-121">DESVPAD (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-122">Calcula o desvio padrão na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="d2166-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-123">QUALQUER (<em>capítulo-alias</em>.<em> nome da coluna</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-p104">Um valor da coluna especificada. ANY possui um valor previsível apenas quando o valor da coluna é igual para todas as linhas do capítulo.
</span><span class="sxs-lookup"><span data-stu-id="d2166-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p>

> [!NOTE]
> <span data-ttu-id="d2166-126">Se a coluna não contiver o mesmo valor para todas as linhas do capítulo, o comando SHAPE retornará arbitrariamente um dos valores para ser o valor da função ANY.</span><span class="sxs-lookup"><span data-stu-id="d2166-126">If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2166-127">Expressão calculada</span><span class="sxs-lookup"><span data-stu-id="d2166-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="d2166-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2166-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2166-129">CALC(<em>expression</em>)</span><span class="sxs-lookup"><span data-stu-id="d2166-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="d2166-p105">Calcula uma expressão arbitrária, mas apenas na linha do <strong>Recordset</strong> que contém a função CALC. Qualquer expressão que usar essas <a href="visual-basic-for-applications-functions.md">Funções do Visual Basic for Applications (VBA)</a> é permitida.</span><span class="sxs-lookup"><span data-stu-id="d2166-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2166-132">Palavra-chave NEW</span><span class="sxs-lookup"><span data-stu-id="d2166-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="d2166-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2166-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2166-134">NOVO <em>tipo de campo</em> [(<em>largura</em> | <em>escala</em> | <em>precisão</em> | <em>erro</em> [, <em>escala</em> | <em>erro</em>])]</span><span class="sxs-lookup"><span data-stu-id="d2166-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="d2166-135">Adiciona ao <strong>Recordset</strong> uma coluna vazia do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="d2166-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d2166-136">O *field-type* passado com a palavra-chave NEW pode ser qualquer um dos tipos de dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2166-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2166-137">Tipos de dados do OLE DB</span><span class="sxs-lookup"><span data-stu-id="d2166-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="d2166-138">Equivalente(s) ao tipo de dados do ADO</span><span class="sxs-lookup"><span data-stu-id="d2166-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2166-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="d2166-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="d2166-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="d2166-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="d2166-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="d2166-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="d2166-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="d2166-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="d2166-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="d2166-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-145">DBTYPE_U1</span><span class="sxs-lookup"><span data-stu-id="d2166-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="d2166-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="d2166-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="d2166-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="d2166-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="d2166-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-149">DBTYPE_U2</span><span class="sxs-lookup"><span data-stu-id="d2166-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="d2166-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="d2166-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-151">DBTYPE_U4</span><span class="sxs-lookup"><span data-stu-id="d2166-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="d2166-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="d2166-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="d2166-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="d2166-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="d2166-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-155">DBTYPE_U8</span><span class="sxs-lookup"><span data-stu-id="d2166-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="d2166-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="d2166-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="d2166-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="d2166-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="d2166-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="d2166-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="d2166-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="d2166-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="d2166-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="d2166-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="d2166-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="d2166-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="d2166-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2166-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="d2166-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="d2166-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="d2166-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="d2166-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="d2166-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="d2166-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="d2166-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="d2166-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="d2166-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="d2166-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="d2166-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="d2166-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="d2166-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="d2166-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="d2166-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2166-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="d2166-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="d2166-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="d2166-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2166-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="d2166-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="d2166-178">adError</span><span class="sxs-lookup"><span data-stu-id="d2166-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d2166-179">Quando o novo campo é do tipo decimal (no OLE DB, DBTYPE\_DECIMAL, ou no ADO, adDecimal), você deve especificar os valores de precisão e escala.</span><span class="sxs-lookup"><span data-stu-id="d2166-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

