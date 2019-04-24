---
title: EventReasonEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293326"
---
# <a name="eventreasonenum"></a>EventReasonEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica a razão que fez com que ocorresse um evento.

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
<td><p><strong>adRsnAddNew</strong></p></td>
<td><p>1</p></td>
<td><p>Uma operação adicionou um novo registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnClose</strong></p></td>
<td><p>241</p></td>
<td><p>Uma operação fechou o <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnDelete</strong></p></td>
<td><p>duas</p></td>
<td><p>Uma operação excluiu um registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnFirstChange</strong></p></td>
<td><p>11</p></td>
<td><p>Uma operação efetuou a primeira alteração em um registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMove</strong></p></td>
<td><p>254</p></td>
<td><p>Uma operação moveu o ponteiro do registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveFirst</strong></p></td>
<td><p>3,6</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o primeiro registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMoveLast</strong></p></td>
<td><p>15</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o último registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveNext</strong></p></td>
<td><p>Treze</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o próximo registro no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMovePrevious</strong></p></td>
<td><p>14</p></td>
<td><p>Uma operação moveu o ponteiro do registro para o registro anterior no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnRequery</strong></p></td>
<td><p>178</p></td>
<td><p>Uma operação consultou novamente o <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnResynch</strong></p></td>
<td><p>8</p></td>
<td><p>Uma operação ressincronizou o <strong>Recordset</strong> ao banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoAddNew</strong></p></td>
<td><p>0,5</p></td>
<td><p>Uma operação inverteu a adição de um novo registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUndoDelete</strong></p></td>
<td><p>6</p></td>
<td><p>Uma operação reverteu a exclusão de um registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoUpdate</strong></p></td>
<td><p>quatro</p></td>
<td><p>Uma operação reverteu a atualização de um registro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUpdate</strong></p></td>
<td><p>3D</p></td>
<td><p>Uma operação atualizou um registro existente.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. EventReason. ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. CLOSE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. DELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. FIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. MOVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. MOVEFIRST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. moVELASt</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. MOVENEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. reQUERy</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. reSYNCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. UNDOADDNEW</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. UNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. UNDOUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. UPDATE</p></td>
</tr>
</tbody>
</table>

