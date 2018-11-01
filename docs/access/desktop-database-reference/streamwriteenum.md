---
title: StreamWriteEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7ba09a0b741483713dfa019062309344eecdb139
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891118"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica se um separador de linha está anexado à string gravada em um objeto [Stream](stream-object-ado.md).

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adWriteChar</strong></p></td>
<td><p>0</p></td>
<td><p>Padrão. Grava a sequência de texto especificada (especificada por parâmetro <em>Data</em>) no objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1</p></td>
<td><p>Grava uma sequência de texto e um caractere de separador de linha em um objeto <strong>Stream</strong>. Se a propriedade <a href="lineseparator-property-ado.md">LineSeparator</a> não for definida, retornará um erro em tempo de execução.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

