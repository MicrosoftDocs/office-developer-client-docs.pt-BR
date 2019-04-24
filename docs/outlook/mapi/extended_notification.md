---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341115"
---
# <a name="extendednotification"></a><span data-ttu-id="34d77-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="34d77-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="34d77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34d77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34d77-105">Descreve informações relacionadas a um evento que é específico do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="34d77-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34d77-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="34d77-106">Header file:</span></span>  <br/> |<span data-ttu-id="34d77-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="34d77-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="34d77-108">Members</span><span class="sxs-lookup"><span data-stu-id="34d77-108">Members</span></span>

 <span data-ttu-id="34d77-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="34d77-109">**ulEvent**</span></span>
  
> <span data-ttu-id="34d77-110">Código de evento estendido definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="34d77-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="34d77-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="34d77-111">**cb**</span></span>
  
> <span data-ttu-id="34d77-112">Contagem de bytes nos parâmetros específicos de eventos apontados por **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="34d77-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="34d77-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="34d77-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="34d77-114">Ponteiro para parâmetros específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="34d77-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="34d77-115">Os tipos de parâmetros usados dependem do valor do membro **ulEvent** ; esses parâmetros são documentados pelo provedor que emitiu o evento.</span><span class="sxs-lookup"><span data-stu-id="34d77-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34d77-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="34d77-116">Remarks</span></span>

<span data-ttu-id="34d77-117">A estrutura **EXTENDED_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="34d77-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="34d77-118">Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **EXTENDED_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="34d77-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="34d77-119">O evento estendido é definido por um provedor de serviços para representar um tipo de alteração que não pode ser abrangido por nenhum dos outros eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="34d77-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="34d77-120">Somente os clientes que conhecem antes eles se registram que um provedor de serviços suporta um evento estendido pode se registrar para esse evento.</span><span class="sxs-lookup"><span data-stu-id="34d77-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="34d77-121">Não é possível para os clientes determinarem sem conhecimento avançado se um provedor de serviços oferecer suporte a um evento estendido.</span><span class="sxs-lookup"><span data-stu-id="34d77-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="34d77-122">Se um provedor de serviços oferecer suporte a um evento estendido, mostrará como lidar com esse evento quando ele for recebido.</span><span class="sxs-lookup"><span data-stu-id="34d77-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="34d77-123">Uma notificação estendida é enviada pela sessão quando um cliente faz logoff.</span><span class="sxs-lookup"><span data-stu-id="34d77-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="34d77-124">Registre-se para esta notificação chamando [IMAPISession:: Advise](imapisession-advise.md) com o parâmetro _lpEntryID_ definido como NULL e o parâmetro _cbEntryID_ definido como zero.</span><span class="sxs-lookup"><span data-stu-id="34d77-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="34d77-125">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="34d77-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="34d77-126">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="34d77-126">**Topic**</span></span>|<span data-ttu-id="34d77-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34d77-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34d77-128">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="34d77-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="34d77-129">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="34d77-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="34d77-130">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="34d77-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="34d77-131">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="34d77-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="34d77-132">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="34d77-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="34d77-133">Discussão sobre como os provedores de serviços podem usar os métodos [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="34d77-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34d77-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="34d77-134">See also</span></span>



[<span data-ttu-id="34d77-135">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="34d77-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="34d77-136">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="34d77-136">MAPI Structures</span></span>](mapi-structures.md)

