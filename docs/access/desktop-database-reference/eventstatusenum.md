---
title: EventStatusEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49f584603c25997e1b01b94f23aaf9f5429a9e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461946"
---
# <a name="eventstatusenum"></a>EventStatusEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica o status atual da execução de um evento.

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
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>4</p></td>
<td><p>Solicita o cancelamento da operação que provocou o evento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>3</p></td>
<td><p>Indica que a operação não pode solicitar o cancelamento da operação pendente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que a operação que provocou o evento falhou devido a um ou mais erros.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que a operação que provocou o evento foi bem-sucedida.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>5</p></td>
<td><p>Impede notificações subsequentes antes que o método de evento tenha terminado a execução.</p></td>
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

