---
title: Tipos de eventos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffb3bd48db4d8071e56553f4ea5bf79b83952466
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463632"
---
# <a name="types-of-events"></a><span data-ttu-id="99e6d-102">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="99e6d-102">Types of Events</span></span>


<span data-ttu-id="99e6d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="99e6d-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="99e6d-p101">Há dois tipos básicos de eventos. Os "eventos Will", chamados antes do início de uma operação, geralmente incluem "Will" nos nomes  por exemplo, **WillChangeRecordset** ou **WillConnect**. Os eventos chamados após a conclusão de um evento geralmente incluem "Complete" nos nomes  por exemplo, **RecordChangeComplete** ou **ConnectComplete**. Há exceções  como no caso de **InfoMessage**  mas elas ocorrem após a conclusão da operação associada.</span><span class="sxs-lookup"><span data-stu-id="99e6d-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="99e6d-108">Eventos Will</span><span class="sxs-lookup"><span data-stu-id="99e6d-108">Will Events</span></span>

<span data-ttu-id="99e6d-109">Os manipuladores de eventos chamados antes do início da operação permitem que você examine ou modifique os parâmetros de operação e, em seguida, cancele a operação ou permita sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="99e6d-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="99e6d-110">Essas rotinas de manipulador de eventos geralmente têm nomes do formulário \**irá*evento \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="99e6d-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="99e6d-111">Eventos Complete</span><span class="sxs-lookup"><span data-stu-id="99e6d-111">Complete Events</span></span>

<span data-ttu-id="99e6d-112">Os manipuladores de eventos chamados após a conclusão de uma operação podem notificar seu aplicativo de que a operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="99e6d-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="99e6d-113">Esse manipulador de eventos também é notificado quando um manipulador de eventos Will cancela uma operação pendente.</span><span class="sxs-lookup"><span data-stu-id="99e6d-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="99e6d-114">Essas rotinas de manipulador de eventos geralmente têm nomes do formulário \***evento \* Complete**.</span><span class="sxs-lookup"><span data-stu-id="99e6d-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="99e6d-115">Os eventos Will e Complete geralmente são usados em pares.</span><span class="sxs-lookup"><span data-stu-id="99e6d-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="99e6d-116">Outros eventos</span><span class="sxs-lookup"><span data-stu-id="99e6d-116">Other Events</span></span>

<span data-ttu-id="99e6d-117">Manipuladores de eventos — ou seja, os eventos cujos nomes não estiverem no formato **será \* evento**\* ou \***evento \* Complete —** são chamados somente quando uma operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="99e6d-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="99e6d-118">Esses eventos são o **Disconnect**, o **EndOfRecordset** e o **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="99e6d-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

