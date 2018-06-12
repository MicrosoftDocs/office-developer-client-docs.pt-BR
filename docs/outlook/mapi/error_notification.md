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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766512"
---
# <a name="errornotification"></a><span data-ttu-id="54614-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="54614-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="54614-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54614-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54614-105">Descreve as informações que se relacionam com um erro crítico.</span><span class="sxs-lookup"><span data-stu-id="54614-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="54614-106">Isso faz com que uma notificação de erro a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="54614-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54614-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="54614-107">Header file:</span></span>  <br/> |<span data-ttu-id="54614-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54614-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="54614-109">Membros</span><span class="sxs-lookup"><span data-stu-id="54614-109">Members</span></span>

 <span data-ttu-id="54614-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="54614-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="54614-111">Contagem de bytes no identificador de entrada apontado pela **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="54614-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="54614-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="54614-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="54614-113">Ponteiro para o identificador de entrada do objeto que faz com que o erro.</span><span class="sxs-lookup"><span data-stu-id="54614-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="54614-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="54614-114">**scode**</span></span>
  
> <span data-ttu-id="54614-115">Valor de erro para o erro crítico.</span><span class="sxs-lookup"><span data-stu-id="54614-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="54614-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="54614-116">**ulFlags**</span></span>
  
> <span data-ttu-id="54614-117">Bitmask dos sinalizadores usados para designar o formato do texto apontado pelo membro **lpszError** na estrutura apontado pela **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="54614-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="54614-118">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="54614-118">The following flag can be set:</span></span>
    
<span data-ttu-id="54614-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54614-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="54614-120">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="54614-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="54614-121">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="54614-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="54614-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="54614-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="54614-123">Ponteiro para uma estrutura [MAPIERROR](mapierror.md) descrevendo o erro.</span><span class="sxs-lookup"><span data-stu-id="54614-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54614-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="54614-124">Remarks</span></span>

<span data-ttu-id="54614-125">A estrutura **ERROR_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="54614-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="54614-126">Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **ERROR_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido para _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="54614-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="54614-127">O valor do membro **cbEntryID** e o membro **lpEntryID** pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="54614-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="54614-128">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="54614-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="54614-129">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="54614-129">**Topic**</span></span>|<span data-ttu-id="54614-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54614-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54614-131">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="54614-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="54614-132">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="54614-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="54614-133">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="54614-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="54614-134">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="54614-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="54614-135">Suporte de notificação de evento</span><span class="sxs-lookup"><span data-stu-id="54614-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="54614-136">Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="54614-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54614-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="54614-137">See also</span></span>



[<span data-ttu-id="54614-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="54614-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="54614-139">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="54614-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="54614-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="54614-140">MAPI Structures</span></span>](mapi-structures.md)

