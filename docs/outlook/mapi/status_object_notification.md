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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336439"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="31360-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="31360-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="31360-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31360-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31360-105">Descreve um objeto de status que foi afetado por uma alteração.</span><span class="sxs-lookup"><span data-stu-id="31360-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31360-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="31360-106">Header file:</span></span>  <br/> |<span data-ttu-id="31360-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="31360-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="31360-108">Members</span><span class="sxs-lookup"><span data-stu-id="31360-108">Members</span></span>

 <span data-ttu-id="31360-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="31360-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="31360-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="31360-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="31360-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="31360-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="31360-112">Ponteiro para o identificador de entrada do objeto status alterado.</span><span class="sxs-lookup"><span data-stu-id="31360-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="31360-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="31360-113">**cValues**</span></span>
  
> <span data-ttu-id="31360-114">Contagem de estruturas [SPropValue](spropvalue.md) na matriz apontada pelo membro **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="31360-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="31360-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="31360-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="31360-116">Ponteiro para uma matriz de estruturas **SPropValue** que descrevem as propriedades do objeto status alterado.</span><span class="sxs-lookup"><span data-stu-id="31360-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31360-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="31360-117">Remarks</span></span>

<span data-ttu-id="31360-118">A estrutura **STATUS_OBJECT_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="31360-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="31360-119">A estrutura **STATUS_OBJECT_NOTIFICATION** é incluída em uma notificação de objeto status para um evento do tipo _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="31360-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="31360-120">Status o objeto Notification é uma notificação de MAPI interno; Os clientes e provedores de serviço não podem se registrar para os provedores de serviços e de ti não podem gerá-lo.</span><span class="sxs-lookup"><span data-stu-id="31360-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="31360-121">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="31360-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="31360-122">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="31360-122">**Topic**</span></span>|<span data-ttu-id="31360-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="31360-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31360-124">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="31360-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="31360-125">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="31360-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="31360-126">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="31360-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="31360-127">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="31360-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="31360-128">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="31360-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="31360-129">Discussão sobre como os provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="31360-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31360-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="31360-130">See also</span></span>



[<span data-ttu-id="31360-131">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="31360-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="31360-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="31360-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="31360-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="31360-133">MAPI Structures</span></span>](mapi-structures.md)

