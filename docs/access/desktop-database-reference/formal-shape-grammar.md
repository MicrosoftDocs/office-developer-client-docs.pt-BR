---
title: Gramática formal de shape
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f226faa303a4ff99a062449548478d32fc60612
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877146"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="6df64-102">Gramática formal de shape</span><span class="sxs-lookup"><span data-stu-id="6df64-102">Formal Shape Grammar</span></span>


<span data-ttu-id="6df64-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6df64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6df64-104">Esta é a gramática formal para a criação de qualquer comando shape:</span><span class="sxs-lookup"><span data-stu-id="6df64-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="6df64-105">Os termos gramaticais necessários são sequências de caracteres de texto delimitadas por colchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="6df64-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="6df64-106">Os termos opcionais são delimitados por colchetes ("\[ \]").</span><span class="sxs-lookup"><span data-stu-id="6df64-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="6df64-107">As alternativas são indicadas por vírgula ("|").</span><span class="sxs-lookup"><span data-stu-id="6df64-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="6df64-108">As alternativas de repetição são indicadas por reticências ("...").</span><span class="sxs-lookup"><span data-stu-id="6df64-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="6df64-109">*Alpha* indica uma cadeia de caracteres de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="6df64-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="6df64-110">*Digit* indica uma cadeia de caracteres de números.</span><span class="sxs-lookup"><span data-stu-id="6df64-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="6df64-111">*Unicode-digit* indica uma cadeia de caracteres de dígitos unicode.</span><span class="sxs-lookup"><span data-stu-id="6df64-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="6df64-112">Todos os outros termos são literais.</span><span class="sxs-lookup"><span data-stu-id="6df64-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6df64-113">Termo</span><span class="sxs-lookup"><span data-stu-id="6df64-113">Term</span></span></p></th>
<th><p><span data-ttu-id="6df64-114">Definição</span><span class="sxs-lookup"><span data-stu-id="6df64-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6df64-115">&lt;comando Shape&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-116">FORMA [&lt;tabela-exp&gt; [[como] &lt;alias&gt;]] [&lt;ação de forma&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-117">&lt;tabela-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-118">{&lt;texto de comando do provedor&gt;} |</span><span class="sxs-lookup"><span data-stu-id="6df64-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="6df64-119">(&lt;comando shape&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="6df64-120">TABELA &lt;nome entre aspas&gt; |</span><span class="sxs-lookup"><span data-stu-id="6df64-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="6df64-121">&lt;nome entre aspas&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-122">&lt;ação da forma&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-123">APPEND &lt;lista de campos com alias&gt; |</span><span class="sxs-lookup"><span data-stu-id="6df64-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="6df64-124">COMPUTE &lt;lista de campos de alias&gt; [BY &lt;lista de campos&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-125">&lt;lista de campos com alias&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-126">&lt;campo alias&gt; [, &lt;campo alias … &gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-127">&lt;campo de alias&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-128">&lt;campo-exp&gt; [[como] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-129">&lt;campo-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-130">(&lt;relation-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-131">&lt;exp calculada&gt; |</span><span class="sxs-lookup"><span data-stu-id="6df64-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="6df64-132">&lt;Aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="6df64-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="6df64-133">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-135">&lt;tabela-exp&gt; [[como] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="6df64-136">&lt;tabela-exp&gt; [[como] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-137">&lt;lista de cond Relation&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-138">&lt;Relation-cond&gt; [, &lt;relation-cond&gt;…]</span><span class="sxs-lookup"><span data-stu-id="6df64-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-139">&lt;Relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-140">&lt;nome do campo&gt; para &lt;filho-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-141">&lt;filho-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-142">&lt;nome do campo&gt; |</span><span class="sxs-lookup"><span data-stu-id="6df64-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="6df64-143">PARÂMETRO &lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-145">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-146">&lt;lista de campos&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-147">&lt;nome do campo&gt; [, &lt;nome do campo&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-148">&lt;Aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-149">Soma (&lt;nome qualificado de campo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-150">AVG (&lt;nome qualificado de campo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-151">MIN (&lt;nome qualificado de campo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-152">MAX (&lt;nome qualificado de campo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-153">CONTAGEM (&lt;qualificado-alias&gt; | &lt;nome qualificado&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-154">DESVPAD (&lt;nome qualificado de campo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="6df64-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="6df64-155">QUALQUER (&lt;nome qualificado de campo&gt;)</span><span class="sxs-lookup"><span data-stu-id="6df64-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-156">&lt;exp calculada&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-157">CALC(&lt;expression&gt;)</span><span class="sxs-lookup"><span data-stu-id="6df64-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-158">&lt;nome qualificado de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-159">&lt;alias&gt;. [&lt;alias&gt;…] &lt;nome do campo&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-161">&lt;nome entre aspas&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-162">&lt;nome do campo&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-163">&lt;nome citados&gt; [[como] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="6df64-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-164">&lt;nome entre aspas&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-165">&quot;&lt;cadeia de caracteres&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="6df64-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="6df64-166">'&lt;cadeia de caracteres&gt;' |</span><span class="sxs-lookup"><span data-stu-id="6df64-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="6df64-167">[&lt;cadeia de caracteres&gt;] |</span><span class="sxs-lookup"><span data-stu-id="6df64-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="6df64-168">&lt;nome&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-169">&lt;nome qualificado&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-170">alias [.alias...]</span><span class="sxs-lookup"><span data-stu-id="6df64-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-171">&lt;nome&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-172">alfa [alfa | dígito | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="6df64-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-173">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-174">Dígito [dígito …]</span><span class="sxs-lookup"><span data-stu-id="6df64-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-175">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-176">NOVO &lt;tipo de campo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</span><span class="sxs-lookup"><span data-stu-id="6df64-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-178">Um tipo de dados ADO ou OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6df64-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df64-179">&lt;cadeia de caracteres&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-180">Unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="6df64-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df64-181">&lt;expressão&gt;</span><span class="sxs-lookup"><span data-stu-id="6df64-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="6df64-182">Uma expressão do Visual Basic for Applications cujos operandos são outras colunas não-CALC na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="6df64-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

