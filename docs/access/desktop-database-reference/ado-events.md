---
title: Eventos de ActiveX Data Objects (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cc2ef73798dca18e00c42768fde78da2abdb56a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706041"
---
# <a name="ado-events"></a><span data-ttu-id="07243-102">Eventos do ADO</span><span class="sxs-lookup"><span data-stu-id="07243-102">ADO events</span></span>

<span data-ttu-id="07243-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="07243-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="07243-104">Evento</span><span class="sxs-lookup"><span data-stu-id="07243-104">Event</span></span></th>
<th><span data-ttu-id="07243-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="07243-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">Eventos BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-107">Chamado após a operação <strong>BeginTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-109">Chamado após a operação <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-111">Chamado após o início da conexão.</span><span class="sxs-lookup"><span data-stu-id="07243-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-112"><a href="connectcomplete-and-disconnect-events-ado.md">Desconectar</a></span><span class="sxs-lookup"><span data-stu-id="07243-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="07243-113">Chamado após o término da conexão.</span><span class="sxs-lookup"><span data-stu-id="07243-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="07243-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="07243-115">Chamado quando há uma tentativa de mover para uma linha além do final do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-117">Chamado após a conclusão da execução de um comando.</span><span class="sxs-lookup"><span data-stu-id="07243-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-119">Chamado após a recuperação de todos os registros em uma operação assíncrona demorada no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="07243-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="07243-121">Chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas foram atualmente recuperadas no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-123">Chamado após a alteração do valor de um ou mais objetos <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-124"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="07243-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="07243-125">Chamado sempre que um aviso ocorre durante a operação <strong>ConnectionEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-127">Chamado após as alterações da posição atual no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-129">Chamado após a alteração de um ou mais registros.</span><span class="sxs-lookup"><span data-stu-id="07243-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-131">Chamado após a alteração do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="07243-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="07243-133">Chamado após a operação <strong>RollbackTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="07243-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="07243-135">Chamado antes que a operação pendente altere o valor de um ou mais objetos <strong>Field</strong> no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="07243-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="07243-137">Chamado antes da alteração de um ou mais registros (linhas) no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="07243-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="07243-139">Chamado antes que uma operação pendente altere o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-140"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="07243-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="07243-141">Chamado antes do início da conexão.</span><span class="sxs-lookup"><span data-stu-id="07243-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07243-142"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="07243-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="07243-143">Chamado um pouco antes da execução de um comando pendente nessa conexão, garantindo ao usuário uma oportunidade de examinar e modificar os parâmetros de execução pendentes.</span><span class="sxs-lookup"><span data-stu-id="07243-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07243-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="07243-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="07243-145">O evento <strong>WillMove</strong> é chamado <em>antes de</em> uma operação pendente altera a posição atual no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="07243-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
