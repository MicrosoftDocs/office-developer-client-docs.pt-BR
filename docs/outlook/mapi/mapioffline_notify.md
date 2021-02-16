---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414764"
---
# <a name="mapioffline_notify"></a><span data-ttu-id="efc0c-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="efc0c-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="efc0c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efc0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efc0c-105">Esta é a notificação para uma alteração no estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="efc0c-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="efc0c-106">Ele indica a parte do estado de conexão que mudou, o estado de conexão antigo e o novo estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="efc0c-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="efc0c-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="efc0c-107">Quick info</span></span>

<span data-ttu-id="efc0c-108">Consulte **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="efc0c-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="efc0c-109">Members</span><span class="sxs-lookup"><span data-stu-id="efc0c-109">Members</span></span>

 <span data-ttu-id="efc0c-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="efc0c-110">_ulSize_</span></span>
  
> <span data-ttu-id="efc0c-111">Tamanho da estrutura **MAPIOFFLINE_NOTIFY** tamanho.</span><span class="sxs-lookup"><span data-stu-id="efc0c-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="efc0c-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="efc0c-112">_NotifyType_</span></span>
  
> <span data-ttu-id="efc0c-113">Tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="efc0c-113">Type of notification.</span></span> <span data-ttu-id="efc0c-114">Observe que somente a notificação sobre a alteração do estado da conexão é suportada; os únicos valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="efc0c-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="efc0c-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="efc0c-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="efc0c-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="efc0c-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="efc0c-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="efc0c-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="efc0c-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="efc0c-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="efc0c-119">Um token definido pelo cliente na estrutura **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="efc0c-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="efc0c-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="efc0c-120">_ulMask_</span></span>
  
> <span data-ttu-id="efc0c-121">A parte do estado de conexão que foi alterada.</span><span class="sxs-lookup"><span data-stu-id="efc0c-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="efc0c-122">O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="efc0c-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="efc0c-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="efc0c-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="efc0c-124">O estado de conexão antigo.</span><span class="sxs-lookup"><span data-stu-id="efc0c-124">The old connection state.</span></span> <span data-ttu-id="efc0c-125">Os únicos valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="efc0c-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="efc0c-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="efc0c-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="efc0c-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="efc0c-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="efc0c-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="efc0c-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="efc0c-129">O novo estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="efc0c-129">The new connection state.</span></span> <span data-ttu-id="efc0c-130">Os únicos valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="efc0c-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="efc0c-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="efc0c-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="efc0c-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="efc0c-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efc0c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="efc0c-133">Remarks</span></span>

<span data-ttu-id="efc0c-134">A API de Estado Offline é compatível apenas com notificações para alterações online/offline.</span><span class="sxs-lookup"><span data-stu-id="efc0c-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="efc0c-135">Um cliente deve verificar se o Outlook retorna os seguintes valores antes de examinar a alteração real:</span><span class="sxs-lookup"><span data-stu-id="efc0c-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="efc0c-136">*NotifyType*  tem o valor MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="efc0c-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="efc0c-137">Nesse caso, o cliente pode assumir que a alteração é uma alteração de estado de conexão, e  *Info*  é da estrutura  *StateChange*  .</span><span class="sxs-lookup"><span data-stu-id="efc0c-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="efc0c-138">*ulMask*  tem o valor MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="efc0c-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="efc0c-139">Nesse caso, o cliente pode presumir que a alteração é uma alteração de estado de conexão online/offline e pode continuar examinando  *ulStateOld*  e  *ulStateNew*  .</span><span class="sxs-lookup"><span data-stu-id="efc0c-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="efc0c-140">É possível que o Outlook notifique um cliente sobre outras alterações que não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="efc0c-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="efc0c-141">Nesses casos, *NotifyType* não seria qualquer um dos três valores declarados anteriormente ou *ulMask* não seria MAPIOFFLINE_STATE_OFFLINE_MASK, e o cliente deve ignorar o restante dos dados em *Informações.*</span><span class="sxs-lookup"><span data-stu-id="efc0c-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efc0c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="efc0c-142">See also</span></span>

- [<span data-ttu-id="efc0c-143">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="efc0c-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="efc0c-144">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="efc0c-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="efc0c-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="efc0c-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

