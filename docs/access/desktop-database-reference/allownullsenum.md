---
title: AllowNullsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: aca4cdb3ae20fa96f40d130ece4ec78540b6e41d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876761"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica se os registros com valores nulos são indexados.

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
<td><p><strong>adIndexNullsAllow</strong></p></td>
<td><p>0</p></td>
<td><p>O índice não permite entradas nas quais as colunas chave são nulas. Se for inserido um valor nulo em uma dessas colunas, a entrada será inserida no índice.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. O índice não permite entradas nas quais as colunas chave são nulas. Se for inserido um valor nulo em uma dessas colunas, ocorrerá um erro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>2</p></td>
<td><p>O índice não insere entradas que contenham chaves nulas. Se for inserido um valor nulo em uma coluna chave, a entrada será ignorada e não ocorrerá nenhum erro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>4</p></td>
<td><p>O índice não insere entradas onde alguma coluna chave contenha um valor nulo. Em um índice com uma chave de várias colunas, se for inserido um valor nulo em alguma coluna, a entrada será ignorada e não ocorrerá nenhum erro.</p></td>
</tr>
</tbody>
</table>

