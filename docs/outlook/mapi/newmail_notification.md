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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326240"
---
# <a name="newmailnotification"></a><span data-ttu-id="9cc33-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cc33-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="9cc33-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cc33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cc33-105">Descreve informações relacionadas à chegada de uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="9cc33-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cc33-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9cc33-106">Header file:</span></span>  <br/> |<span data-ttu-id="9cc33-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9cc33-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="9cc33-108">Members</span><span class="sxs-lookup"><span data-stu-id="9cc33-108">Members</span></span>

 <span data-ttu-id="9cc33-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="9cc33-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="9cc33-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="9cc33-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="9cc33-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="9cc33-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="9cc33-112">Ponteiro para o identificador de entrada da mensagem recém-criada.</span><span class="sxs-lookup"><span data-stu-id="9cc33-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="9cc33-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="9cc33-113">**cbParentID**</span></span>
  
> <span data-ttu-id="9cc33-114">Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="9cc33-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="9cc33-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="9cc33-115">**lpParentID**</span></span>
  
> <span data-ttu-id="9cc33-116">Ponteiro para o identificador de entrada da pasta de recebimento da mensagem recém-criada.</span><span class="sxs-lookup"><span data-stu-id="9cc33-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="9cc33-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9cc33-117">**ulFlags**</span></span>
  
> <span data-ttu-id="9cc33-118">Bitmask dos sinalizadores usados para descrever o formato das propriedades de cadeia de caracteres incluídas na mensagem.</span><span class="sxs-lookup"><span data-stu-id="9cc33-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="9cc33-119">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9cc33-119">The following flag can be set:</span></span>
    
<span data-ttu-id="9cc33-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9cc33-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9cc33-121">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9cc33-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9cc33-122">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9cc33-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9cc33-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="9cc33-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="9cc33-124">Ponteiro para a classe de mensagem da mensagem que chegou recentemente.</span><span class="sxs-lookup"><span data-stu-id="9cc33-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="9cc33-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="9cc33-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="9cc33-126">Bitmask de sinalizadores que descreve o estado atual da mensagem que acabou de chegar.</span><span class="sxs-lookup"><span data-stu-id="9cc33-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="9cc33-127">O membro **ulMessageFlags** é uma cópia da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9cc33-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9cc33-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cc33-128">Remarks</span></span>

<span data-ttu-id="9cc33-129">A estrutura **NEWMAIL_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="9cc33-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="9cc33-130">Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **NEWMAIL_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="9cc33-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="9cc33-131">MAPI usa a estrutura **NEWMAIL_NOTIFICATION** somente como membro da estrutura de **notificação** , que contém informações sobre um evento de notificação para o coletor de aviso.</span><span class="sxs-lookup"><span data-stu-id="9cc33-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="9cc33-132">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cc33-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="9cc33-133">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="9cc33-133">**Topic**</span></span>|<span data-ttu-id="9cc33-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9cc33-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cc33-135">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="9cc33-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="9cc33-136">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="9cc33-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="9cc33-137">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="9cc33-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="9cc33-138">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="9cc33-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="9cc33-139">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="9cc33-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="9cc33-140">Discussão sobre como os provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="9cc33-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cc33-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cc33-141">See also</span></span>



[<span data-ttu-id="9cc33-142">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cc33-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="9cc33-143">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="9cc33-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="9cc33-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9cc33-144">MAPI Structures</span></span>](mapi-structures.md)

