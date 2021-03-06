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
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>Funções de agregação, a função CALC e a palavra-chave NEW


**Aplica-se ao:** Access 2013, Office 2013

A técnica data shaping oferece suporte para as funções a seguir. O nome atribuído ao capítulo que contém a coluna a ser operada é o *chapter-alias*.

Um chapter-alias pode ser totalmente qualificado, consistindo no nome de coluna de cada capítulo, levando ao capítulo que contém o *column-name*, todos separados por pontos. Por exemplo, se o capítulo pai, chap1, contiver um capítulo filho, chap2, que tenha uma coluna de quantidade, amt, então o nome qualificado será chap1.chap2.amt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Funções agregadas</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SUM(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula a soma de todos os valores da coluna especificada.</p></td>
</tr>
<tr class="even">
<td><p>AVG(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula a média de todos os valores da coluna especificada.</p></td>
</tr>
<tr class="odd">
<td><p>MAX(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula o valor máximo na coluna especificada.</p></td>
</tr>
<tr class="even">
<td><p>MIN(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula o valor mínimo na coluna especificada.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT(<em>chapter-alias</em>[.<em> column-name</em>])</p></td>
<td><p>Conta o número de linhas no alias especificado. Se uma coluna for especificada, somente as linhas para as quais essa coluna for não-Null serão incluídas na contagem.</p></td>
</tr>
<tr class="even">
<td><p>STDEV(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula o desvio padrão na coluna especificada.</p></td>
</tr>
<tr class="odd">
<td><p>ANY(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Um valor da coluna especificada. ANY possui um valor previsível apenas quando o valor da coluna é igual para todas as linhas do capítulo.</p><p><strong>OBSERVAÇÃO:</strong>se a coluna não contém o mesmo valor para todas as linhas no capítulo, o comando SHAPE retorna arbitrariamente um dos valores para ser o valor da função ANY.</p></td>
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
<th><p>Expressão calculada</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC(<em>expressão</em>)</p></td>
<td><p>Calcula uma expressão arbitrária, mas apenas na linha do <strong>Recordset</strong> que contém a função CALC. Qualquer expressão que usar essas <a href="visual-basic-for-applications-functions.md">Funções do Visual Basic for Applications (VBA)</a> é permitida.</p></td>
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
<th><p>Palavra-chave NEW</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NEW <em>field-type</em> [(<em>width</em>  |  <em>scale</em>  |  <em>precision</em>  |  <em>error</em> [, <em>scale</em>  |  <em>error</em>])]</p></td>
<td><p>Adiciona ao <strong>Recordset</strong> uma coluna vazia do tipo especificado.</p></td>
</tr>
</tbody>
</table>

<br/>

O *field-type* passado com a palavra-chave NEW pode ser qualquer um dos tipos de dados a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipos de dados do OLE DB</p></th>
<th><p>Equivalente(s) ao tipo de dados do ADO</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>adBSTR</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adBoolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adUnsignedTinyInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adTinyInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adUnsignedSmallInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adUnsignedInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adBigInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adUnsignedBigInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adGuid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>adBinary, AdVarBinary, adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>adChar, adVarChar, adLongVarChar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>adWChar, adVarWChar, adLongVarWChar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>adDBDate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>adDBTime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>adDBTimeStamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adFileTime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>adError</p></td>
</tr>
</tbody>
</table>


Quando o novo campo for do tipo decimal (em OLE DB, DBTYPE DECIMAL ou \_ em ADO, adDecimal), você deverá especificar os valores de precisão e escala.

