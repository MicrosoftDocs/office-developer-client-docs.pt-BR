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

  - Os termos opcionais são delimitados por colchetes\[ \]("").

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
<td><p>&lt;forma-comando&gt;</p></td>
<td><p>Forma [&lt;Table-exp&gt; [[as] &lt;alias&gt;]] [&lt;forma-ação&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;tabela-exp&gt;</p></td>
<td><p>{&lt;Provider-Command-Text&gt;} |<br />
(&lt;forma-comando&gt;) |<br />
TABELA &lt;-nome entre aspas&gt; |<br />
&lt;nome entre aspas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;forma-ação&gt;</p></td>
<td><p>ACRESCENTAR &lt;com alias-lista de campos&gt; |</p>
<p>COMPUTE &lt;alias-Field-List&gt; [by &lt;field-list]&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias-lista de campos&gt;</p></td>
<td><p>&lt;alias-Field&gt; [, &lt;aliasd-Field... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;alias-Field&gt;</p></td>
<td><p>&lt;Field-exp&gt; [[as] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Field-exp&gt;</p></td>
<td><p>(&lt;relation-exp&gt;) |</p>
<p>&lt;calculado-exp&gt; |</p>
<p>&lt;Aggregate-exp&gt; |</p>
<p>&lt;New-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;Table-exp&gt; [[as] &lt;alias&gt;]</p>
<p>&lt;Table-exp&gt; [[as] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-List&gt;</p></td>
<td><p>&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;campo-nome&gt; para &lt;filho-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;filho-ref&gt;</p></td>
<td><p>&lt;nome do campo&gt; |</p>
<p>PARÂMETRO &lt;param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;série&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos&gt;</p></td>
<td><p>&lt;campo-nome&gt; [, &lt;nome&gt;do campo]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aggregate-exp&gt;</p></td>
<td><p>SUM (&lt;Qualified-Field-Name&gt;) |</p>
<p>Méd (&lt;Qualified-Field-Name&gt;) |</p>
<p>MIN (&lt;Qualified-Field-Name&gt;) |</p>
<p>MAX (&lt;Qualified-Field-Name&gt;) |</p>
<p>Count (&lt;Qualified-alias&gt; | &lt;Qualified-name&gt;) |</p>
<p>Desv (&lt;Qualified-Field-Name&gt;) |</p>
<p>QUALQUER (&lt;Qualified-Field-Name&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculado-exp&gt;</p></td>
<td><p>CALC (&lt;expressão&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-Field-Name&gt;</p></td>
<td><p>&lt;alias&gt;. [&lt;alias&gt;...] &lt;nome do campo&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alternativos&gt;</p></td>
<td><p>&lt;nome entre aspas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nome do campo&gt;</p></td>
<td><p>&lt;quot-name&gt; [[as] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nome entre aspas&gt;</p></td>
<td><p>&quot;&lt;sequência&gt;&quot; |</p>
<p>'&lt;cadeia&gt;de caracteres ' |</p>
<p>[&lt;cadeia&gt;de caracteres] |</p>
<p>&lt;tdomínio&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-Name&gt;</p></td>
<td><p>alias [. alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;tdomínio&gt;</p></td>
<td><p>Alpha [Alpha | digit | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;série&gt;</p></td>
<td><p>digit [dígito...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;New-exp&gt;</p></td>
<td><p>Novo &lt;campo-tipo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;tipo de campo&gt;</p></td>
<td><p>Um tipo de dados ADO ou OLE DB.</p></td>
</tr>
<tr class="even">
<td><p>&lt;sequência&gt;</p></td>
<td><p>Unicode-Char [Unicode-Char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expressão&gt;</p></td>
<td><p>Uma expressão do Visual Basic for Applications cujos operandos são outras colunas não-CALC na mesma linha.</p></td>
</tr>
</tbody>
</table>

