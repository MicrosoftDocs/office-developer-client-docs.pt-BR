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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766527"
---
# <a name="extendednotification"></a><span data-ttu-id="23749-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="23749-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="23749-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23749-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23749-105">Descreve as informações relacionadas a um evento que é específico do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="23749-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23749-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="23749-106">Header file:</span></span>  <br/> |<span data-ttu-id="23749-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23749-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="23749-108">Membros</span><span class="sxs-lookup"><span data-stu-id="23749-108">Members</span></span>

 <span data-ttu-id="23749-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="23749-109">**ulEvent**</span></span>
  
> <span data-ttu-id="23749-110">Código de evento estendidas que é definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="23749-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="23749-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="23749-111">**cb**</span></span>
  
> <span data-ttu-id="23749-112">Contagem de bytes nos parâmetros específicos do evento apontado pela **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="23749-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="23749-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="23749-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="23749-114">Ponteiro para os parâmetros de eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="23749-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="23749-115">O tipo de parâmetros que são usados depende do valor do membro **ulEvent** ; Esses parâmetros são documentados pelo provedor que emitiu o evento.</span><span class="sxs-lookup"><span data-stu-id="23749-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="23749-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="23749-116">Remarks</span></span>

<span data-ttu-id="23749-117">A estrutura **EXTENDED_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="23749-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="23749-118">Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **EXTENDED_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido para _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="23749-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="23749-119">O evento estendido é definido por um provedor de serviços para representar um tipo de alteração que não pode ser coberto por qualquer um dos outros eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="23749-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="23749-120">Somente os clientes que saber antes de se registram que um provedor de serviços oferece suporte a um evento estendido podem se inscrever para o evento.</span><span class="sxs-lookup"><span data-stu-id="23749-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="23749-121">Não é possível para os clientes determinar sem o conhecimento avançado, se um evento estendido oferece suporte a um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="23749-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="23749-122">Se um provedor de serviços oferece suporte a um evento estendido, ele mostra como lidar com esse evento quando ele for recebido.</span><span class="sxs-lookup"><span data-stu-id="23749-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="23749-123">Uma notificação estendida é enviada da sessão quando um cliente fizer logoff.</span><span class="sxs-lookup"><span data-stu-id="23749-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="23749-124">Registre-se para essa notificação chamando [IMAPISession::Advise](imapisession-advise.md) com o parâmetro _lpEntryID_ definido como NULL e o parâmetro _cbEntryID_ definido como zero.</span><span class="sxs-lookup"><span data-stu-id="23749-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="23749-125">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="23749-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="23749-126">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="23749-126">**Topic**</span></span>|<span data-ttu-id="23749-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23749-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23749-128">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="23749-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="23749-129">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="23749-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="23749-130">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="23749-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="23749-131">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="23749-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="23749-132">Suporte de notificação de evento</span><span class="sxs-lookup"><span data-stu-id="23749-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="23749-133">Discussão sobre como provedores de serviços podem usar os métodos [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="23749-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23749-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="23749-134">See also</span></span>



[<span data-ttu-id="23749-135">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="23749-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="23749-136">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="23749-136">MAPI Structures</span></span>](mapi-structures.md)

