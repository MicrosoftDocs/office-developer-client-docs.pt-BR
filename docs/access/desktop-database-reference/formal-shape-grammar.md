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
# <a name="formal-shape-grammar"></a>Gramática formal de forma

**Aplica-se ao:** Access 2013, Office 2013

Esta é a gramática formal para a criação de qualquer comando shape:

  - Os termos gramaticais necessários são sequências de caracteres de texto delimitadas por colchetes angulares ("\<\>").

  - Os termos opcionais são delimitados por colchetes (" \[ \] ").

  - As alternativas são indicadas por vírgula ("|").

  - As alternativas de repetição são indicadas por reticências ("...").

  - *Alpha* indica uma sequência de caracteres de letras alfabéticas.

  - *Digit* indica uma sequência de caracteres de números.

  - *Unicode-digit* indica uma sequência de caracteres de dígitos unicode.

Todos os outros termos são literais.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Termo</p></th>
<th><p>Definição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;shape-command&gt;</p></td>
<td><p>SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{ &lt; provider-command-text &gt; } |<br />
( &lt; comando de forma ) &gt; |<br />
TABLE &lt; quoted-name&gt; |<br />
&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;shape-action&gt;</p></td>
<td><p>APPEND &lt; aliased-field-list&gt; |</p>
<p>COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aliased-field&gt;</p></td>
<td><p>&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-exp&gt;</p></td>
<td><p>( &lt; relation-exp &gt; ) |</p>
<p>&lt;calculated-exp&gt; |</p>
<p>&lt;aggregate-exp&gt; |</p>
<p>&lt;new-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p>
<p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-list&gt;</p></td>
<td><p>&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;field-name &gt; TO &lt; child-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;child-ref&gt;</p></td>
<td><p>&lt;field-name&gt; |</p>
<p>PARAMETER &lt; param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;number&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-list&gt;</p></td>
<td><p>&lt;field-name &gt; [, &lt; field-name &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>SOMA( &lt; qualified-field-name &gt; ) |</p>
<p>Nome de campo qualificado ( &lt; &gt; AVG) |</p>
<p>Min( &lt; qualified-field-name &gt; ) |</p>
<p>MAX( &lt; qualified-field-name &gt; ) |</p>
<p>COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</p>
<p>STDEV( &lt; qualified-field-name &gt; ) |</p>
<p>ANY( &lt; qualified-field-name &gt; )</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC( &lt; expressão &gt; )</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-field-name&gt;</p></td>
<td><p>&lt;alias &gt; .[ &lt; alias &gt; ...] &lt; field-name&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;field-name&gt;</p></td>
<td><p>&lt;quoted-name &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;quoted-name&gt;</p></td>
<td><p>&quot;&lt;string&gt;&quot; |</p>
<p>' &lt; string &gt; ' |</p>
<p>[ &lt; cadeia &gt; de caracteres ] |</p>
<p>&lt;nome&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-name&gt;</p></td>
<td><p>alias[.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nome&gt;</p></td>
<td><p>alfa [ alfa | dígito | _ | # | : | ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;number&gt;</p></td>
<td><p>dígito [dígito...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;tipo de campo&gt;</p></td>
<td><p>Um tipo de dados ADO ou OLE DB.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expressão&gt;</p></td>
<td><p>Uma expressão do Visual Basic for Applications cujos operandos são outras colunas não-CALC na mesma linha.</p></td>
</tr>
</tbody>
</table>

