---
title: Resumo do manipulador de eventos do ADO
TOCTitle: ADO Event Handler Summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e47cf076c213707857285757d936d58bd153e7c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880597"
---
# <a name="ado-event-handler-summary"></a>Resumo do manipulador de eventos do ADO


**Aplica-se a**: Access 2013, o Office 2013

Dois objetos do ADO podem gerar eventos: o objeto [Connection](connection-object-ado.md) e o objeto [Recordset](recordset-object-ado.md). A família **ConnectionEvent** pertence às operações no objeto **Connection**, e a família **RecordsetEvent** pertence às operações no objeto **Recordset**.

  - **Eventos Connection**: os eventos são emitidos quando uma transação é iniciada em uma conexão, é confirmada ou revertida; quando um [Comando](command-object-ado.md) é executado; quando ocorre um aviso durante uma operação **Connection Event**; ou quando uma **Conexão** é iniciada ou finalizada.

  - **Eventos Recordset**: os eventos são emitidos em operações de busca assíncrona e quando você navega pelas linhas de um objeto **Recordset**, altera um campo em uma linha de um **Recordset**, altera uma linha em um **Recordset**, abre um **Recordset** com um cursor de servidor, fecha um **Recordset** ou faz uma alteração no **Recordset**.

As seguintes tabelas resumem os eventos e suas descrições.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">Eventos BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>Gerenciamento de transação</strong> — Notificação sobre o início, a confirmação ou a reversão da transação atual na conexão.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, desconecte</a></p></td>
<td><p><strong>Gerenciamento de conexão</strong> — Notificação informando que a conexão atual será iniciada, foi iniciada ou foi finalizada.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>Gerenciamento de execução de comandos</strong> — Notificação informando que a execução do comando atual na conexão será iniciada ou foi finalizada.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Informativa</strong> — Notificação sobre a existência de informações adicionais sobre a operação atual.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>RecordsetEvent</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p><strong>Status de recuperação</strong> — Notificação do progresso de uma operação de recuperação de dados ou da conclusão da operação de recuperação. Esses eventos estarão disponíveis somente se <strong>Recordset</strong>  tiver sido aberto com a utilização de um curso do cliente.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></p></td>
<td><p><strong>Gerenciamento de alterações do campo</strong> — Notificação informando que o valor do campo atual será alterado ou foi alterado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>Gerenciamento de navegação</strong> — Notificação informando que a posição atual da linha em um <strong>Recordset</strong> será alterada, foi alterada ou atingiu o final do <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></p></td>
<td><p><strong>Gerenciamento de alteração de linha</strong> — Notificação informando que algo na linha atual do <strong>Recordset</strong> será alterado ou foi alterado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></p></td>
<td><p><strong>Gerenciamento de alteração de Recordset</strong> — Notificação informando que algo no <strong>Recordset</strong> será alterado ou foi alterado.</p></td>
</tr>
</tbody>
</table>

