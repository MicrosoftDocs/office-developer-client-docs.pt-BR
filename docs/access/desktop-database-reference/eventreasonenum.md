---
title: EventReasonEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec32b47d8e69c065d167fe86553aafdec906bc24
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462038"
---
# <a name="eventreasonenum"></a>EventReasonEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica a razão que fez com que ocorresse um evento.

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
<td><p><strong>adRsnAddNew</strong></p></td>
<td><p>1</p></td>
<td><p>Uma operação adicionou um novo registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnClose</strong></p></td>
<td><p>9</p></td>
<td><p>Uma operação fechou o <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnDelete</strong></p></td>
<td><p>2</p></td>
<td><p>Uma operação excluiu um registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnFirstChange</strong></p></td>
<td><p>11</p></td>
<td><p>Uma operação efetuou a primeira alteração em um registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMove</strong></p></td>
<td><p>10</p></td>
<td><p>Uma operação moveu o ponteiro do registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveFirst</strong></p></td>
<td><p>12</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o primeiro registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMoveLast</strong></p></td>
<td><p>15</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o último registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveNext</strong></p></td>
<td><p>13</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o próximo registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMovePrevious</strong></p></td>
<td><p>14</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o registro anterior no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnRequery</strong></p></td>
<td><p>7</p></td>
<td><p>Uma operação consultou novamente o <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnResynch</strong></p></td>
<td><p>8</p></td>
<td><p>Uma operação ressincronizou o <strong>Recordset</strong> ao banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoAddNew</strong></p></td>
<td><p>5</p></td>
<td><p>Uma operação inverteu a adição de um novo registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUndoDelete</strong></p></td>
<td><p>6</p></td>
<td><p>Uma operação reverteu a exclusão de um registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoUpdate</strong></p></td>
<td><p>4</p></td>
<td><p>Uma operação reverteu a atualização de um registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUpdate</strong></p></td>
<td><p>3</p></td>
<td><p>Uma operação atualizou um registro existente.</p></td>
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
<td><p>AdoEnums.EventReason.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.CLOSE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.DELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.FIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.MOVEFIRST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVELAST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.MOVENEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.REQUERY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.RESYNCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.UNDOADDNEW</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.UNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.UNDOUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.UPDATE</p></td>
</tr>
</tbody>
</table>
