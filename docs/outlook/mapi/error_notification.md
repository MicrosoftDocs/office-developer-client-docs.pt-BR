---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425439"
---
# <a name="errornotification"></a><span data-ttu-id="80d83-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="80d83-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="80d83-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80d83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80d83-105">Descreve informações relacionadas a um erro crítico.</span><span class="sxs-lookup"><span data-stu-id="80d83-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="80d83-106">Isso faz com que uma notificação de erro seja gerada.</span><span class="sxs-lookup"><span data-stu-id="80d83-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80d83-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="80d83-107">Header file:</span></span>  <br/> |<span data-ttu-id="80d83-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="80d83-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a><span data-ttu-id="80d83-109">Members</span><span class="sxs-lookup"><span data-stu-id="80d83-109">Members</span></span>

 <span data-ttu-id="80d83-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="80d83-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="80d83-111">Contagem de bytes no identificador de entrada apontado por **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="80d83-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="80d83-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="80d83-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="80d83-113">Ponteiro para o identificador de entrada do objeto que causa o erro.</span><span class="sxs-lookup"><span data-stu-id="80d83-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="80d83-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="80d83-114">**scode**</span></span>
  
> <span data-ttu-id="80d83-115">Valor de erro para o erro crítico.</span><span class="sxs-lookup"><span data-stu-id="80d83-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="80d83-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="80d83-116">**ulFlags**</span></span>
  
> <span data-ttu-id="80d83-117">Bitmask dos sinalizadores usados para designar o formato do texto apontado pelo membro **lpszError** na estrutura indicada por **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="80d83-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="80d83-118">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="80d83-118">The following flag can be set:</span></span>
    
<span data-ttu-id="80d83-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80d83-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="80d83-120">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="80d83-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="80d83-121">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="80d83-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="80d83-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="80d83-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="80d83-123">Ponteiro para uma estrutura [MAPIERROR](mapierror.md) descrevendo o erro.</span><span class="sxs-lookup"><span data-stu-id="80d83-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="80d83-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="80d83-124">Remarks</span></span>

<span data-ttu-id="80d83-125">A estrutura **ERROR_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="80d83-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="80d83-126">Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **ERROR_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="80d83-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="80d83-127">O valor do membro **cbEntryID** e o membro **lpEntryID** podem ser nulos.</span><span class="sxs-lookup"><span data-stu-id="80d83-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="80d83-128">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80d83-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="80d83-129">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="80d83-129">**Topic**</span></span>|<span data-ttu-id="80d83-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d83-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80d83-131">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="80d83-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="80d83-132">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="80d83-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="80d83-133">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="80d83-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="80d83-134">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="80d83-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="80d83-135">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="80d83-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="80d83-136">Discussão sobre como os provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="80d83-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80d83-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="80d83-137">See also</span></span>



[<span data-ttu-id="80d83-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="80d83-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="80d83-139">Notifica</span><span class="sxs-lookup"><span data-stu-id="80d83-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="80d83-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="80d83-140">MAPI Structures</span></span>](mapi-structures.md)

