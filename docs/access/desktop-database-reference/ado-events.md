---
title: Eventos do ActiveX Data Objects (ADO)
TOCTitle: ADO Events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d7a885d5fdd7736a37c2f195c3bf14b4af8a70d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876229"
---
# <a name="ado-events"></a><span data-ttu-id="efdf0-102">Eventos do ADO</span><span class="sxs-lookup"><span data-stu-id="efdf0-102">ADO Events</span></span>


<span data-ttu-id="efdf0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="efdf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">Eventos BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-105">Chamado após a operação <strong>BeginTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-105">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-107">Chamado após a operação <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-107">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-109">Chamado após o início da conexão.</span><span class="sxs-lookup"><span data-stu-id="efdf0-109">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-110"><a href="connectcomplete-and-disconnect-events-ado.md">Desconectar</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-110"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-111">Chamado após o término da conexão.</span><span class="sxs-lookup"><span data-stu-id="efdf0-111">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-113">Chamado quando há uma tentativa de mover para uma linha além do final do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-113">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-115">Chamado após a conclusão da execução de um comando.</span><span class="sxs-lookup"><span data-stu-id="efdf0-115">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-117">Chamado após a recuperação de todos os registros em uma operação assíncrona demorada no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-117">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-119">Chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas foram atualmente recuperadas no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-119">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-121">Chamado após a alteração do valor de um ou mais objetos <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-121">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-122"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-122"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-123">Chamado sempre que um aviso ocorre durante a operação <strong>ConnectionEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-123">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-125">Chamado após as alterações da posição atual no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-125">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-127">Chamado após a alteração de um ou mais registros.</span><span class="sxs-lookup"><span data-stu-id="efdf0-127">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-129">Chamado após a alteração do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-129">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-131">Chamado após a operação <strong>RollbackTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-131">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-133">Chamado antes que a operação pendente altere o valor de um ou mais objetos <strong>Field</strong> no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-133">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-135">Chamado antes da alteração de um ou mais registros (linhas) no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-135">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-137">Chamado antes que uma operação pendente altere o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-137">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-138"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-138"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-139">Chamado antes do início da conexão.</span><span class="sxs-lookup"><span data-stu-id="efdf0-139">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efdf0-140"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-140"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-141">Chamado um pouco antes da execução de um comando pendente nessa conexão, garantindo ao usuário uma oportunidade de examinar e modificar os parâmetros de execução pendentes.</span><span class="sxs-lookup"><span data-stu-id="efdf0-141">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efdf0-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="efdf0-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="efdf0-143">O evento <strong>WillMove</strong> é chamado <em>antes de</em> uma operação pendente altera a posição atual no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="efdf0-143">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

