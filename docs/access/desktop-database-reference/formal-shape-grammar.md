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
# <a name="formal-shape-grammar"></a><span data-ttu-id="79c8a-102">Gramática formal de forma</span><span class="sxs-lookup"><span data-stu-id="79c8a-102">Formal shape grammar</span></span>

<span data-ttu-id="79c8a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79c8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79c8a-104">Esta é a gramática formal para a criação de qualquer comando shape:</span><span class="sxs-lookup"><span data-stu-id="79c8a-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="79c8a-105">Os termos gramaticais necessários são sequências de caracteres de texto delimitadas por colchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="79c8a-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="79c8a-106">Os termos opcionais são delimitados por colchetes\[ \]("").</span><span class="sxs-lookup"><span data-stu-id="79c8a-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="79c8a-107">As alternativas são indicadas por vírgula ("|").</span><span class="sxs-lookup"><span data-stu-id="79c8a-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="79c8a-108">As alternativas de repetição são indicadas por reticências ("...").</span><span class="sxs-lookup"><span data-stu-id="79c8a-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="79c8a-109">*Alpha* indica uma sequência de caracteres de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="79c8a-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="79c8a-110">*Digit* indica uma sequência de caracteres de números.</span><span class="sxs-lookup"><span data-stu-id="79c8a-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="79c8a-111">*Unicode-digit* indica uma sequência de caracteres de dígitos unicode.</span><span class="sxs-lookup"><span data-stu-id="79c8a-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="79c8a-112">Todos os outros termos são literais.</span><span class="sxs-lookup"><span data-stu-id="79c8a-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79c8a-113">Termo</span><span class="sxs-lookup"><span data-stu-id="79c8a-113">Term</span></span></p></th>
<th><p><span data-ttu-id="79c8a-114">Definição</span><span class="sxs-lookup"><span data-stu-id="79c8a-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-115">&lt;forma-comando&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-116">Forma [&lt;Table-exp&gt; [[as] &lt;alias&gt;]] [&lt;forma-ação&gt;]</span><span class="sxs-lookup"><span data-stu-id="79c8a-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-117">&lt;tabela-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-118">{&lt;Provider-Command-Text&gt;} |</span><span class="sxs-lookup"><span data-stu-id="79c8a-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="79c8a-119">(&lt;forma-comando&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="79c8a-120">TABELA &lt;-nome entre aspas&gt; |</span><span class="sxs-lookup"><span data-stu-id="79c8a-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="79c8a-121">&lt;nome entre aspas&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-122">&lt;forma-ação&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-123">ACRESCENTAR &lt;com alias-lista de campos&gt; |</span><span class="sxs-lookup"><span data-stu-id="79c8a-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="79c8a-124">COMPUTE &lt;alias-Field-List&gt; [by &lt;field-list]&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-125">&lt;alias-lista de campos&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-126">&lt;alias-Field&gt; [, &lt;aliasd-Field... &gt;]</span><span class="sxs-lookup"><span data-stu-id="79c8a-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-127">&lt;alias-Field&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-128">&lt;Field-exp&gt; [[as] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="79c8a-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-129">&lt;Field-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-130">(&lt;relation-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-131">&lt;calculado-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="79c8a-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="79c8a-132">&lt;Aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="79c8a-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="79c8a-133">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-135">&lt;Table-exp&gt; [[as] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="79c8a-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="79c8a-136">&lt;Table-exp&gt; [[as] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="79c8a-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-137">&lt;relation-cond-List&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="79c8a-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-140">&lt;campo-nome&gt; para &lt;filho-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-141">&lt;filho-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-142">&lt;nome do campo&gt; |</span><span class="sxs-lookup"><span data-stu-id="79c8a-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="79c8a-143">PARÂMETRO &lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-145">&lt;série&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-146">&lt;lista de campos&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-147">&lt;campo-nome&gt; [, &lt;nome&gt;do campo]</span><span class="sxs-lookup"><span data-stu-id="79c8a-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-148">&lt;Aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-149">SUM (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-150">Méd (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-151">MIN (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-152">MAX (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-153">Count (&lt;Qualified-alias&gt; | &lt;Qualified-name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-154">Desv (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="79c8a-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="79c8a-155">QUALQUER (&lt;Qualified-Field-Name&gt;)</span><span class="sxs-lookup"><span data-stu-id="79c8a-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-156">&lt;calculado-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-157">CALC (&lt;expressão&gt;)</span><span class="sxs-lookup"><span data-stu-id="79c8a-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-158">&lt;qualified-Field-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-159">&lt;alias&gt;. [&lt;alias&gt;...] &lt;nome do campo&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-160">&lt;alternativos&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-161">&lt;nome entre aspas&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-162">&lt;nome do campo&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-163">&lt;quot-name&gt; [[as] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="79c8a-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-164">&lt;nome entre aspas&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-165">&quot;&lt;sequência&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="79c8a-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="79c8a-166">'&lt;cadeia&gt;de caracteres ' |</span><span class="sxs-lookup"><span data-stu-id="79c8a-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="79c8a-167">[&lt;cadeia&gt;de caracteres] |</span><span class="sxs-lookup"><span data-stu-id="79c8a-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="79c8a-168">&lt;tdomínio&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-169">&lt;qualified-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-170">alias [. alias...]</span><span class="sxs-lookup"><span data-stu-id="79c8a-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-171">&lt;tdomínio&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-172">Alpha [Alpha | digit | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="79c8a-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-173">&lt;série&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-174">digit [dígito...]</span><span class="sxs-lookup"><span data-stu-id="79c8a-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-175">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-176">Novo &lt;campo-tipo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</span><span class="sxs-lookup"><span data-stu-id="79c8a-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-178">Um tipo de dados ADO ou OLE DB.</span><span class="sxs-lookup"><span data-stu-id="79c8a-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8a-179">&lt;sequência&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-180">Unicode-Char [Unicode-Char...]</span><span class="sxs-lookup"><span data-stu-id="79c8a-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8a-181">&lt;expressão&gt;</span><span class="sxs-lookup"><span data-stu-id="79c8a-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="79c8a-182">Uma expressão do Visual Basic for Applications cujos operandos são outras colunas não-CALC na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="79c8a-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

