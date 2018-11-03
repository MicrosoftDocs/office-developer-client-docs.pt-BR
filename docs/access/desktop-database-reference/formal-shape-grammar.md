---
title: Gramática formal de shape
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de4f2eca0b5dd607cb9d93cc7e90f4af0ba8d89
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945534"
---
# <a name="formal-shape-grammar"></a>Gramática formal de shape

**Aplica-se a**: Access 2013, o Office 2013

Esta é a gramática formal para a criação de qualquer comando shape:

  - Os termos gramaticais necessários são sequências de caracteres de texto delimitadas por colchetes angulares ("\<\>").

  - Os termos opcionais são delimitados por colchetes ("\[ \]").

  - As alternativas são indicadas por vírgula ("|").

  - As alternativas de repetição são indicadas por reticências ("...").

  - *Alpha* indica uma cadeia de caracteres de letras alfabéticas.

  - *Digit* indica uma cadeia de caracteres de números.

  - *Unicode-digit* indica uma cadeia de caracteres de dígitos unicode.

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
<td><p>&lt;comando Shape&gt;</p></td>
<td><p>FORMA [&lt;tabela-exp&gt; [[como] &lt;alias&gt;]] [&lt;ação de forma&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;tabela-exp&gt;</p></td>
<td><p>{&lt;texto de comando do provedor&gt;} |<br />
(&lt;comando shape&gt;) |<br />
TABELA &lt;nome entre aspas&gt; |<br />
&lt;nome entre aspas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;ação da forma&gt;</p></td>
<td><p>APPEND &lt;lista de campos com alias&gt; |</p>
<p>COMPUTE &lt;lista de campos de alias&gt; [BY &lt;lista de campos&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos com alias&gt;</p></td>
<td><p>&lt;campo alias&gt; [, &lt;campo alias … &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;campo de alias&gt;</p></td>
<td><p>&lt;campo-exp&gt; [[como] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;campo-exp&gt;</p></td>
<td><p>(&lt;relation-exp&gt;) |</p>
<p>&lt;exp calculada&gt; |</p>
<p>&lt;Aggregate-exp&gt; |</p>
<p>&lt;New-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;tabela-exp&gt; [[como] &lt;alias&gt;]</p>
<p>&lt;tabela-exp&gt; [[como] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de cond Relation&gt;</p></td>
<td><p>&lt;Relation-cond&gt; [, &lt;relation-cond&gt;…]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Relation-cond&gt;</p></td>
<td><p>&lt;nome do campo&gt; para &lt;filho-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;filho-ref&gt;</p></td>
<td><p>&lt;nome do campo&gt; |</p>
<p>PARÂMETRO &lt;param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;número&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos&gt;</p></td>
<td><p>&lt;nome do campo&gt; [, &lt;nome do campo&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aggregate-exp&gt;</p></td>
<td><p>Soma (&lt;nome qualificado de campo&gt;) |</p>
<p>AVG (&lt;nome qualificado de campo&gt;) |</p>
<p>MIN (&lt;nome qualificado de campo&gt;) |</p>
<p>MAX (&lt;nome qualificado de campo&gt;) |</p>
<p>CONTAGEM (&lt;qualificado-alias&gt; | &lt;nome qualificado&gt;) |</p>
<p>DESVPAD (&lt;nome qualificado de campo&gt;) |</p>
<p>QUALQUER (&lt;nome qualificado de campo&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;exp calculada&gt;</p></td>
<td><p>CALC(&lt;expression&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nome qualificado de campo&gt;</p></td>
<td><p>&lt;alias&gt;. [&lt;alias&gt;…] &lt;nome do campo&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;nome entre aspas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nome do campo&gt;</p></td>
<td><p>&lt;nome citados&gt; [[como] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nome entre aspas&gt;</p></td>
<td><p>&quot;&lt;cadeia de caracteres&gt;&quot; |</p>
<p>'&lt;cadeia de caracteres&gt;' |</p>
<p>[&lt;cadeia de caracteres&gt;] |</p>
<p>&lt;nome&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nome qualificado&gt;</p></td>
<td><p>alias [.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nome&gt;</p></td>
<td><p>alfa [alfa | dígito | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;número&gt;</p></td>
<td><p>Dígito [dígito …]</p></td>
</tr>
<tr class="even">
<td><p>&lt;New-exp&gt;</p></td>
<td><p>NOVO &lt;tipo de campo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;tipo de campo&gt;</p></td>
<td><p>Um tipo de dados ADO ou OLE DB.</p></td>
</tr>
<tr class="even">
<td><p>&lt;cadeia de caracteres&gt;</p></td>
<td><p>Unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expressão&gt;</p></td>
<td><p>Uma expressão do Visual Basic for Applications cujos operandos são outras colunas não-CALC na mesma linha.</p></td>
</tr>
</tbody>
</table>

