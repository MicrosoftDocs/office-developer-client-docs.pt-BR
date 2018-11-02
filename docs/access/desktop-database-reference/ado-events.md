---
title: Eventos de ActiveX Data Objects (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cc8ac02e2410a2f7bfe1038851e16f50c1ea2ee
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910940"
---
# <a name="ado-events"></a><span data-ttu-id="62a9b-102">Eventos do ADO</span><span class="sxs-lookup"><span data-stu-id="62a9b-102">ADO events</span></span>

<span data-ttu-id="62a9b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="62a9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="62a9b-104">Evento</span><span class="sxs-lookup"><span data-stu-id="62a9b-104">Event</span></span></th>
<th><span data-ttu-id="62a9b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="62a9b-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">Eventos BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-107">Chamado após a operação <strong>BeginTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-109">Chamado após a operação <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-111">Chamado após o início da conexão.</span><span class="sxs-lookup"><span data-stu-id="62a9b-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-112"><a href="connectcomplete-and-disconnect-events-ado.md">Desconectar</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-113">Chamado após o término da conexão.</span><span class="sxs-lookup"><span data-stu-id="62a9b-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-115">Chamado quando há uma tentativa de mover para uma linha além do final do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-117">Chamado após a conclusão da execução de um comando.</span><span class="sxs-lookup"><span data-stu-id="62a9b-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-119">Chamado após a recuperação de todos os registros em uma operação assíncrona demorada no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-121">Chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas foram atualmente recuperadas no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-123">Chamado após a alteração do valor de um ou mais objetos <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-124"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-125">Chamado sempre que um aviso ocorre durante a operação <strong>ConnectionEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-127">Chamado após as alterações da posição atual no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-129">Chamado após a alteração de um ou mais registros.</span><span class="sxs-lookup"><span data-stu-id="62a9b-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-131">Chamado após a alteração do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-133">Chamado após a operação <strong>RollbackTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-135">Chamado antes que a operação pendente altere o valor de um ou mais objetos <strong>Field</strong> no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-137">Chamado antes da alteração de um ou mais registros (linhas) no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-139">Chamado antes que uma operação pendente altere o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-140"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-141">Chamado antes do início da conexão.</span><span class="sxs-lookup"><span data-stu-id="62a9b-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a9b-142"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-143">Chamado um pouco antes da execução de um comando pendente nessa conexão, garantindo ao usuário uma oportunidade de examinar e modificar os parâmetros de execução pendentes.</span><span class="sxs-lookup"><span data-stu-id="62a9b-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a9b-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="62a9b-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="62a9b-145">O evento <strong>WillMove</strong> é chamado <em>antes de</em> uma operação pendente altera a posição atual no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62a9b-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>