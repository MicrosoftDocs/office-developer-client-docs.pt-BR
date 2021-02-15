---
title: Gramática formal de forma
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292318"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="076cd-102">Gramática formal de forma</span><span class="sxs-lookup"><span data-stu-id="076cd-102">Formal shape grammar</span></span>

<span data-ttu-id="076cd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="076cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="076cd-104">Esta é a gramática formal para a criação de qualquer comando shape:</span><span class="sxs-lookup"><span data-stu-id="076cd-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="076cd-105">Os termos gramaticais necessários são sequências de caracteres de texto delimitadas por colchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="076cd-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="076cd-106">Os termos opcionais são delimitados por colchetes (" \[ \] ").</span><span class="sxs-lookup"><span data-stu-id="076cd-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="076cd-107">As alternativas são indicadas por vírgula ("|").</span><span class="sxs-lookup"><span data-stu-id="076cd-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="076cd-108">As alternativas de repetição são indicadas por reticências ("...").</span><span class="sxs-lookup"><span data-stu-id="076cd-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="076cd-109">*Alpha* indica uma sequência de caracteres de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="076cd-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="076cd-110">*Digit* indica uma sequência de caracteres de números.</span><span class="sxs-lookup"><span data-stu-id="076cd-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="076cd-111">*Unicode-digit* indica uma sequência de caracteres de dígitos unicode.</span><span class="sxs-lookup"><span data-stu-id="076cd-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="076cd-112">Todos os outros termos são literais.</span><span class="sxs-lookup"><span data-stu-id="076cd-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="076cd-113">Termo</span><span class="sxs-lookup"><span data-stu-id="076cd-113">Term</span></span></p></th>
<th><p><span data-ttu-id="076cd-114">Definição</span><span class="sxs-lookup"><span data-stu-id="076cd-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="076cd-115">&lt;shape-command&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-116">SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-118">{ &lt; provider-command-text &gt; } |</span><span class="sxs-lookup"><span data-stu-id="076cd-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="076cd-119">( &lt; comando de forma ) &gt; |</span><span class="sxs-lookup"><span data-stu-id="076cd-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="076cd-120">TABLE &lt; quoted-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="076cd-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="076cd-121">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-122">&lt;shape-action&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-123">APPEND &lt; aliased-field-list&gt; |</span><span class="sxs-lookup"><span data-stu-id="076cd-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="076cd-124">COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-125">&lt;aliased-field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-126">&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-127">&lt;aliased-field&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-128">&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-129">&lt;field-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-130">( &lt; relation-exp &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="076cd-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-131">&lt;calculated-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="076cd-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="076cd-132">&lt;aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="076cd-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="076cd-133">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-135">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="076cd-136">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-137">&lt;relation-cond-list&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-138">&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</span><span class="sxs-lookup"><span data-stu-id="076cd-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-140">&lt;field-name &gt; TO &lt; child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-141">&lt;child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-142">&lt;field-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="076cd-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="076cd-143">PARAMETER &lt; param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-145">&lt;number&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-146">&lt;field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-147">&lt;field-name &gt; [, &lt; field-name &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-148">&lt;aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-149">SOMA( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="076cd-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-150">Nome de campo qualificado ( &lt; &gt; AVG) |</span><span class="sxs-lookup"><span data-stu-id="076cd-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-151">Min( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="076cd-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-152">MAX( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="076cd-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-153">COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="076cd-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-154">STDEV( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="076cd-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="076cd-155">ANY( &lt; qualified-field-name &gt; )</span><span class="sxs-lookup"><span data-stu-id="076cd-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-156">&lt;calculated-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-157">CALC( &lt; expressão &gt; )</span><span class="sxs-lookup"><span data-stu-id="076cd-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-158">&lt;qualified-field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-159">&lt;alias &gt; .[ &lt; alias &gt; ...] &lt; field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-161">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-162">&lt;field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-163">&lt;quoted-name &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="076cd-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-164">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-165">&quot;&lt;string&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="076cd-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="076cd-166">' &lt; string &gt; ' |</span><span class="sxs-lookup"><span data-stu-id="076cd-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="076cd-167">[ &lt; cadeia &gt; de caracteres ] |</span><span class="sxs-lookup"><span data-stu-id="076cd-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="076cd-168">&lt;nome&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-169">&lt;qualified-name&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-170">alias[.alias...]</span><span class="sxs-lookup"><span data-stu-id="076cd-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-171">&lt;nome&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-172">alfa [ alfa | dígito | _ | # | : | ...]</span><span class="sxs-lookup"><span data-stu-id="076cd-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-173">&lt;number&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-174">dígito [dígito...]</span><span class="sxs-lookup"><span data-stu-id="076cd-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-175">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-176">NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</span><span class="sxs-lookup"><span data-stu-id="076cd-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-178">Um tipo de dados ADO ou OLE DB.</span><span class="sxs-lookup"><span data-stu-id="076cd-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076cd-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-180">unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="076cd-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076cd-181">&lt;expressão&gt;</span><span class="sxs-lookup"><span data-stu-id="076cd-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="076cd-182">Uma expressão do Visual Basic for Applications cujos operandos são outras colunas não-CALC na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="076cd-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

