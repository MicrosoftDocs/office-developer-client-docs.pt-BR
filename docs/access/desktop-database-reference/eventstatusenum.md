---
title: EventStatusEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293270"
---
# <a name="eventstatusenum"></a>EventStatusEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o status atual da execução de um evento.

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
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>4 </p></td>
<td><p>Solicita o cancelamento da operação que provocou o evento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>3 </p></td>
<td><p>Indica que a operação não pode solicitar o cancelamento da operação pendente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>2 </p></td>
<td><p>Indica que a operação que provocou o evento falhou devido a um ou mais erros.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>1 </p></td>
<td><p>Indica que a operação que provocou o evento foi bem-sucedida.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>5 </p></td>
<td><p>Impede notificações subsequentes antes que o método de evento tenha terminado a execução.</p></td>
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
<td><p>AdoEnums.EventStatus.CANCEL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventStatus.CANTDENY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventStatus.ERRORSOCCURRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventStatus.OK</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventStatus.UNWANTEDEVENT</p></td>
</tr>
</tbody>
</table>

