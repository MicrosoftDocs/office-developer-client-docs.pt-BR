---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439853"
---
# <a name="newmail_notification"></a><span data-ttu-id="fe20a-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="fe20a-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="fe20a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe20a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe20a-105">Descreve informações relacionadas à chegada de uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe20a-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe20a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fe20a-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe20a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe20a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="fe20a-108">Members</span><span class="sxs-lookup"><span data-stu-id="fe20a-108">Members</span></span>

 <span data-ttu-id="fe20a-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="fe20a-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="fe20a-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="fe20a-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="fe20a-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="fe20a-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="fe20a-112">Ponteiro para o identificador de entrada da mensagem recém-chegada.</span><span class="sxs-lookup"><span data-stu-id="fe20a-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="fe20a-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="fe20a-113">**cbParentID**</span></span>
  
> <span data-ttu-id="fe20a-114">Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="fe20a-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="fe20a-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="fe20a-115">**lpParentID**</span></span>
  
> <span data-ttu-id="fe20a-116">Ponteiro para o identificador de entrada da pasta de recebimento da mensagem recém-chegada.</span><span class="sxs-lookup"><span data-stu-id="fe20a-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="fe20a-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="fe20a-117">**ulFlags**</span></span>
  
> <span data-ttu-id="fe20a-118">Bitmask de sinalizadores usados para descrever o formato das propriedades de cadeia de caracteres incluídas na mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe20a-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="fe20a-119">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="fe20a-119">The following flag can be set:</span></span>
    
<span data-ttu-id="fe20a-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fe20a-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fe20a-121">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="fe20a-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="fe20a-122">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="fe20a-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="fe20a-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="fe20a-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="fe20a-124">Ponteiro para a classe de mensagem da mensagem recém-chegada.</span><span class="sxs-lookup"><span data-stu-id="fe20a-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="fe20a-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="fe20a-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="fe20a-126">Bitmask de sinalizadores que descreve o estado atual da mensagem recém-chegada.</span><span class="sxs-lookup"><span data-stu-id="fe20a-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="fe20a-127">O **membro ulMessageFlags** é uma cópia da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe20a-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe20a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe20a-128">Remarks</span></span>

<span data-ttu-id="fe20a-129">A **NEWMAIL_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="fe20a-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="fe20a-130">Quando o **membro de** informações de uma estrutura **NOTIFICATION** contém uma estrutura **NEWMAIL_NOTIFICATION,** o membro **ulEventType** da estrutura **NOTIFICATION** é definido como  _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="fe20a-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="fe20a-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span><span class="sxs-lookup"><span data-stu-id="fe20a-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="fe20a-132">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe20a-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="fe20a-133">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="fe20a-133">**Topic**</span></span>|<span data-ttu-id="fe20a-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe20a-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe20a-135">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="fe20a-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="fe20a-136">Visão geral dos eventos de notificação e notificação.</span><span class="sxs-lookup"><span data-stu-id="fe20a-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="fe20a-137">Manipulando notificações</span><span class="sxs-lookup"><span data-stu-id="fe20a-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="fe20a-138">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="fe20a-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="fe20a-139">Suporte à notificação de evento</span><span class="sxs-lookup"><span data-stu-id="fe20a-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="fe20a-140">Discussão sobre como os provedores de serviços podem usar o [método IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="fe20a-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe20a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe20a-141">See also</span></span>



[<span data-ttu-id="fe20a-142">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="fe20a-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="fe20a-143">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="fe20a-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="fe20a-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="fe20a-144">MAPI Structures</span></span>](mapi-structures.md)

