---
title: Tipos de eventos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718137"
---
# <a name="types-of-events"></a><span data-ttu-id="ecdca-102">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="ecdca-102">Types of events</span></span>


<span data-ttu-id="ecdca-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecdca-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ecdca-p101">Há dois tipos básicos de eventos. Os "eventos Will", chamados antes do início de uma operação, geralmente incluem "Will" nos nomes  por exemplo, **WillChangeRecordset** ou **WillConnect**. Os eventos chamados após a conclusão de um evento geralmente incluem "Complete" nos nomes  por exemplo, **RecordChangeComplete** ou **ConnectComplete**. Há exceções  como no caso de **InfoMessage**  mas elas ocorrem após a conclusão da operação associada.</span><span class="sxs-lookup"><span data-stu-id="ecdca-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="ecdca-108">Eventos Will</span><span class="sxs-lookup"><span data-stu-id="ecdca-108">Will Events</span></span>

<span data-ttu-id="ecdca-109">Os manipuladores de eventos chamados antes do início da operação permitem que você examine ou modifique os parâmetros de operação e, em seguida, cancele a operação ou permita sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="ecdca-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="ecdca-110">Essas rotinas de manipulador de eventos geralmente têm nomes do formulário \**irá*evento \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="ecdca-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="ecdca-111">Eventos Complete</span><span class="sxs-lookup"><span data-stu-id="ecdca-111">Complete Events</span></span>

<span data-ttu-id="ecdca-112">Os manipuladores de eventos chamados após a conclusão de uma operação podem notificar seu aplicativo de que a operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="ecdca-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="ecdca-113">Esse manipulador de eventos também é notificado quando um manipulador de eventos Will cancela uma operação pendente.</span><span class="sxs-lookup"><span data-stu-id="ecdca-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="ecdca-114">Essas rotinas de manipulador de eventos geralmente têm nomes do formulário \***evento \* Complete**.</span><span class="sxs-lookup"><span data-stu-id="ecdca-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="ecdca-115">Os eventos Will e Complete geralmente são usados em pares.</span><span class="sxs-lookup"><span data-stu-id="ecdca-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="ecdca-116">Outros eventos</span><span class="sxs-lookup"><span data-stu-id="ecdca-116">Other Events</span></span>

<span data-ttu-id="ecdca-117">Manipuladores de eventos — ou seja, os eventos cujos nomes não estiverem no formato **será \* evento**\* ou \***evento \* Complete —** são chamados somente quando uma operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="ecdca-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="ecdca-118">Esses eventos são o **Disconnect**, o **EndOfRecordset** e o **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="ecdca-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

