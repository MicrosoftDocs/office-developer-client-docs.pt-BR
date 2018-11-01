---
title: CompareEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 4749064e938912c459f455e54702460339994c37
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874570"
---
# <a name="compareenum"></a>CompareEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica a posição relativa de dois registros representados por seus indicadores.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCompareEqual</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que os indicadores são iguais.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareGreaterThan</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o primeiro indicador é após o segundo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareLessThan</strong></p></td>
<td><p>0</p></td>
<td><p>Indica que o primeiro indicador é antes do segundo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareNotComparable</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que os indicadores não podem ser comparados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareNotEqual</strong></p></td>
<td><p>3</p></td>
<td><p>Indica que os indicadores não são iguais e não estão em ordem.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Compare.EQUAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Compare.GREATERTHAN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Compare.LESSTHAN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Compare.NOTCOMPARABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Compare.NOTEQUAL</p></td>
</tr>
</tbody>
</table>

