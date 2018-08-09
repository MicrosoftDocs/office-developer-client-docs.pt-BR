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
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768148"
---
# <a name="newmailnotification"></a><span data-ttu-id="9909d-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9909d-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="9909d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9909d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9909d-105">Descreve as informações que se relacionam com a chegada de uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="9909d-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9909d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9909d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9909d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9909d-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="9909d-108">Members</span><span class="sxs-lookup"><span data-stu-id="9909d-108">Members</span></span>

 <span data-ttu-id="9909d-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="9909d-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="9909d-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="9909d-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="9909d-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="9909d-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="9909d-112">Ponteiro para o identificador de entrada da mensagem chegar recentemente.</span><span class="sxs-lookup"><span data-stu-id="9909d-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="9909d-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="9909d-113">**cbParentID**</span></span>
  
> <span data-ttu-id="9909d-114">Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="9909d-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="9909d-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="9909d-115">**lpParentID**</span></span>
  
> <span data-ttu-id="9909d-116">Ponteiro para o identificador de entrada da pasta de recebimento da mensagem que acabou de chegar.</span><span class="sxs-lookup"><span data-stu-id="9909d-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="9909d-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9909d-117">**ulFlags**</span></span>
  
> <span data-ttu-id="9909d-118">Bitmask dos sinalizadores usados para descrever o formato das propriedades de cadeia de caracteres incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="9909d-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="9909d-119">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9909d-119">The following flag can be set:</span></span>
    
<span data-ttu-id="9909d-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9909d-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9909d-121">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9909d-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9909d-122">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9909d-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9909d-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="9909d-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="9909d-124">Ponteiro para a classe de mensagem da mensagem chegar recentemente.</span><span class="sxs-lookup"><span data-stu-id="9909d-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="9909d-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="9909d-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="9909d-126">Bitmask dos sinalizadores que descreve o estado atual da mensagem chegar recentemente.</span><span class="sxs-lookup"><span data-stu-id="9909d-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="9909d-127">O membro **ulMessageFlags** é uma cópia de propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9909d-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9909d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="9909d-128">Remarks</span></span>

<span data-ttu-id="9909d-129">A estrutura **NEWMAIL_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="9909d-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="9909d-130">Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **NEWMAIL_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="9909d-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="9909d-131">MAPI usa a estrutura **NEWMAIL_NOTIFICATION** somente como um membro da estrutura de **notificação** , que mantém informações sobre um evento de notificação para o coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="9909d-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="9909d-132">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9909d-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="9909d-133">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="9909d-133">**Topic**</span></span>|<span data-ttu-id="9909d-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9909d-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9909d-135">Notificações de eventos no MAPI</span><span class="sxs-lookup"><span data-stu-id="9909d-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="9909d-136">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="9909d-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="9909d-137">Lidar com notificações</span><span class="sxs-lookup"><span data-stu-id="9909d-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="9909d-138">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="9909d-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="9909d-139">Suporte à notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="9909d-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="9909d-140">Discussão sobre como provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="9909d-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9909d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9909d-141">See also</span></span>



[<span data-ttu-id="9909d-142">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="9909d-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="9909d-143">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="9909d-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="9909d-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9909d-144">MAPI Structures</span></span>](mapi-structures.md)

