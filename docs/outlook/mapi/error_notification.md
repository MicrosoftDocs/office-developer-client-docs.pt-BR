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
ms.openlocfilehash: 2405799fa59abf58583553f8e2d3718d68411a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574969"
---
# <a name="errornotification"></a><span data-ttu-id="b4a21-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b4a21-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="b4a21-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4a21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4a21-105">Descreve as informações que se relacionam com um erro crítico.</span><span class="sxs-lookup"><span data-stu-id="b4a21-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="b4a21-106">Isso faz com que uma notificação de erro a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="b4a21-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4a21-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b4a21-107">Header file:</span></span>  <br/> |<span data-ttu-id="b4a21-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4a21-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="b4a21-109">Members</span><span class="sxs-lookup"><span data-stu-id="b4a21-109">Members</span></span>

 <span data-ttu-id="b4a21-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="b4a21-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="b4a21-111">Contagem de bytes no identificador de entrada apontado pela **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="b4a21-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="b4a21-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="b4a21-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="b4a21-113">Ponteiro para o identificador de entrada do objeto que faz com que o erro.</span><span class="sxs-lookup"><span data-stu-id="b4a21-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="b4a21-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="b4a21-114">**scode**</span></span>
  
> <span data-ttu-id="b4a21-115">Valor de erro para o erro crítico.</span><span class="sxs-lookup"><span data-stu-id="b4a21-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="b4a21-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b4a21-116">**ulFlags**</span></span>
  
> <span data-ttu-id="b4a21-117">Bitmask dos sinalizadores usados para designar o formato do texto apontado pelo membro **lpszError** na estrutura apontado pela **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="b4a21-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="b4a21-118">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="b4a21-118">The following flag can be set:</span></span>
    
<span data-ttu-id="b4a21-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4a21-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b4a21-120">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b4a21-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b4a21-121">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b4a21-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b4a21-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="b4a21-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="b4a21-123">Ponteiro para uma estrutura [MAPIERROR](mapierror.md) descrevendo o erro.</span><span class="sxs-lookup"><span data-stu-id="b4a21-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b4a21-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4a21-124">Remarks</span></span>

<span data-ttu-id="b4a21-125">A estrutura **ERROR_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a21-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b4a21-126">Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **ERROR_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido para _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="b4a21-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="b4a21-127">O valor do membro **cbEntryID** e o membro **lpEntryID** pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b4a21-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="b4a21-128">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4a21-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b4a21-129">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="b4a21-129">**Topic**</span></span>|<span data-ttu-id="b4a21-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b4a21-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4a21-131">Notificações de eventos no MAPI</span><span class="sxs-lookup"><span data-stu-id="b4a21-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b4a21-132">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="b4a21-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b4a21-133">Lidar com notificações</span><span class="sxs-lookup"><span data-stu-id="b4a21-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b4a21-134">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="b4a21-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b4a21-135">Suporte à notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="b4a21-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b4a21-136">Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="b4a21-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4a21-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a21-137">See also</span></span>



[<span data-ttu-id="b4a21-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b4a21-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b4a21-139">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="b4a21-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="b4a21-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b4a21-140">MAPI Structures</span></span>](mapi-structures.md)

