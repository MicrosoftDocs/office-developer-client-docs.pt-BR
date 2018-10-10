---
title: CompareEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9cef64707cb2797c6ad4f1090749779f147c87f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463234"
---
# <a name="compareenum"></a>CompareEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica a posição relativa de dois registros representados por seus indicadores.

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


**ADO/WFC Equivalente**

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

