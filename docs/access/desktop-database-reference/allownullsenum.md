---
title: AllowNullsEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297162"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**Aplica-se ao:** Access 2013, Office 2013

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
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adIndexNullsAllow</strong></p></td>
<td><p>,0</p></td>
<td><p>O índice não permite entradas nas quais as colunas chave são nulas. Se for inserido um valor nulo em uma dessas colunas, a entrada será inserida no índice.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. O índice não permite entradas nas quais as colunas chave são nulas. Se for inserido um valor nulo em uma dessas colunas, ocorrerá um erro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>duas</p></td>
<td><p>O índice não insere entradas que contenham chaves nulas. Se for inserido um valor nulo em uma coluna chave, a entrada será ignorada e não ocorrerá nenhum erro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>quatro</p></td>
<td><p>O índice não insere entradas onde alguma coluna chave contenha um valor nulo. Em um índice com uma chave de várias colunas, se for inserido um valor nulo em alguma coluna, a entrada será ignorada e não ocorrerá nenhum erro.</p></td>
</tr>
</tbody>
</table>

