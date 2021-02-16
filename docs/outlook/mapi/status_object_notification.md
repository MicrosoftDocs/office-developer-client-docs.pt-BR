---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426265"
---
# <a name="status_object_notification"></a><span data-ttu-id="c8518-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c8518-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c8518-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8518-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8518-105">Descreve um objeto de status que foi afetado por uma alteração.</span><span class="sxs-lookup"><span data-stu-id="c8518-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8518-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c8518-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8518-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8518-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="c8518-108">Members</span><span class="sxs-lookup"><span data-stu-id="c8518-108">Members</span></span>

 <span data-ttu-id="c8518-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c8518-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c8518-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="c8518-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c8518-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c8518-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c8518-112">Ponteiro para o identificador de entrada do objeto de status alterado.</span><span class="sxs-lookup"><span data-stu-id="c8518-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="c8518-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c8518-113">**cValues**</span></span>
  
> <span data-ttu-id="c8518-114">Contagem de [estruturas SPropValue](spropvalue.md) na matriz apontada pelo membro **lpPropVals.**</span><span class="sxs-lookup"><span data-stu-id="c8518-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="c8518-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="c8518-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="c8518-116">Ponteiro para uma matriz de **estruturas SPropValue** que descrevem as propriedades do objeto de status alterado.</span><span class="sxs-lookup"><span data-stu-id="c8518-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8518-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8518-117">Remarks</span></span>

<span data-ttu-id="c8518-118">A **STATUS_OBJECT_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="c8518-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c8518-119">A **STATUS_OBJECT_NOTIFICATION** estrutura é incluída com uma notificação de objeto de status para um evento do tipo  _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="c8518-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="c8518-120">Notificação de objeto de status é uma notificação MAPI interna; clientes e provedores de serviços não podem se registrar para ele e os provedores de serviços não podem gerá-lo.</span><span class="sxs-lookup"><span data-stu-id="c8518-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="c8518-121">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8518-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c8518-122">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="c8518-122">**Topic**</span></span>|<span data-ttu-id="c8518-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8518-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8518-124">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="c8518-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c8518-125">Visão geral dos eventos de notificação e notificação.</span><span class="sxs-lookup"><span data-stu-id="c8518-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c8518-126">Manipulando notificações</span><span class="sxs-lookup"><span data-stu-id="c8518-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c8518-127">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="c8518-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c8518-128">Suporte à notificação de evento</span><span class="sxs-lookup"><span data-stu-id="c8518-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c8518-129">Discussão sobre como os provedores de serviços podem usar o **método IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="c8518-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8518-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8518-130">See also</span></span>



[<span data-ttu-id="c8518-131">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="c8518-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c8518-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c8518-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c8518-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c8518-133">MAPI Structures</span></span>](mapi-structures.md)

