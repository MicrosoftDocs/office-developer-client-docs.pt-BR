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
# <a name="ado-event-handler-summary"></a><span data-ttu-id="25e19-102">Resumo do manipulador de eventos do ADO</span><span class="sxs-lookup"><span data-stu-id="25e19-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="25e19-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="25e19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25e19-p101">Dois objetos do ADO podem gerar eventos: o objeto [Connection](connection-object-ado.md) e o objeto [Recordset](recordset-object-ado.md). A família **ConnectionEvent** pertence às operações no objeto **Connection**, e a família **RecordsetEvent** pertence às operações no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="25e19-p101">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object. The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

  - <span data-ttu-id="25e19-106">**Eventos Connection**: os eventos são emitidos quando uma transação é iniciada em uma conexão, é confirmada ou revertida; quando um [Comando](command-object-ado.md) é executado; quando ocorre um aviso durante uma operação **Connection Event**; ou quando uma **Conexão** é iniciada ou finalizada.</span><span class="sxs-lookup"><span data-stu-id="25e19-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

  - <span data-ttu-id="25e19-107">**Eventos Recordset**: os eventos são emitidos em operações de busca assíncrona e quando você navega pelas linhas de um objeto **Recordset**, altera um campo em uma linha de um **Recordset**, altera uma linha em um **Recordset**, abre um **Recordset** com um cursor de servidor, fecha um **Recordset** ou faz uma alteração no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="25e19-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="25e19-108">As seguintes tabelas resumem os eventos e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="25e19-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25e19-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="25e19-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="25e19-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="25e19-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25e19-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">Eventos BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="25e19-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="25e19-112"><strong>Gerenciamento de transação</strong> — Notificação sobre o início, a confirmação ou a reversão da transação atual na conexão.</span><span class="sxs-lookup"><span data-stu-id="25e19-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e19-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, desconecte</a></span><span class="sxs-lookup"><span data-stu-id="25e19-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-114"><strong>Gerenciamento de conexão</strong> — Notificação informando que a conexão atual será iniciada, foi iniciada ou foi finalizada.</span><span class="sxs-lookup"><span data-stu-id="25e19-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e19-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="25e19-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-116"><strong>Gerenciamento de execução de comandos</strong> — Notificação informando que a execução do comando atual na conexão será iniciada ou foi finalizada.</span><span class="sxs-lookup"><span data-stu-id="25e19-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e19-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="25e19-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-118"><strong>Informativa</strong> — Notificação sobre a existência de informações adicionais sobre a operação atual.</span><span class="sxs-lookup"><span data-stu-id="25e19-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="25e19-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="25e19-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="25e19-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="25e19-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25e19-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="25e19-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-p102"><strong>Status de recuperação</strong> — Notificação do progresso de uma operação de recuperação de dados ou da conclusão da operação de recuperação. Esses eventos estarão disponíveis somente se <strong>Recordset</strong>  tiver sido aberto com a utilização de um curso do cliente.</span><span class="sxs-lookup"><span data-stu-id="25e19-p102"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed. These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e19-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="25e19-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-125"><strong>Gerenciamento de alterações do campo</strong> — Notificação informando que o valor do campo atual será alterado ou foi alterado.</span><span class="sxs-lookup"><span data-stu-id="25e19-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e19-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="25e19-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-127"><strong>Gerenciamento de navegação</strong> — Notificação informando que a posição atual da linha em um <strong>Recordset</strong> será alterada, foi alterada ou atingiu o final do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="25e19-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25e19-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="25e19-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-129"><strong>Gerenciamento de alteração de linha</strong> — Notificação informando que algo na linha atual do <strong>Recordset</strong> será alterado ou foi alterado.</span><span class="sxs-lookup"><span data-stu-id="25e19-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25e19-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="25e19-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="25e19-131"><strong>Gerenciamento de alteração de Recordset</strong> — Notificação informando que algo no <strong>Recordset</strong> será alterado ou foi alterado.</span><span class="sxs-lookup"><span data-stu-id="25e19-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

