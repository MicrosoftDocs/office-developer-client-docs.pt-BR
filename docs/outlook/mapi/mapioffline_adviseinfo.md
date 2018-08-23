---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565092"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="48a3d-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="48a3d-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="48a3d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48a3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48a3d-105">Fornece informações para **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** para registrar o retorno de chamada para um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="48a3d-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="48a3d-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="48a3d-106">Quick info</span></span>

<span data-ttu-id="48a3d-107">Consulte **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="48a3d-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a><span data-ttu-id="48a3d-108">Members</span><span class="sxs-lookup"><span data-stu-id="48a3d-108">Members</span></span>

<span data-ttu-id="48a3d-109">_ulSize_: O tamanho do **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="48a3d-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="48a3d-110">_ulClientToken_: um token definido pelo cliente sobre um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="48a3d-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="48a3d-111">É o membro *ulClientToken* da estrutura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** passado para **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="48a3d-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="48a3d-112">_CallbackType_: tipo de retorno de chamada para fazer.</span><span class="sxs-lookup"><span data-stu-id="48a3d-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="48a3d-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="48a3d-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="48a3d-114">O tipo de retorno de chamada é por notificação.</span><span class="sxs-lookup"><span data-stu-id="48a3d-114">The type of callback is by notification.</span></span> <span data-ttu-id="48a3d-115">Este é o único tipo com suporte de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="48a3d-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="48a3d-116">*pCallback* deve indicar a interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="48a3d-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="48a3d-117">_pCallback_: Interface para usar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="48a3d-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="48a3d-118">Esta é a implementação do cliente de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="48a3d-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="48a3d-119">_ulAdviseTypes_: os tipos de advise, conforme identificado pela condição para que informa.</span><span class="sxs-lookup"><span data-stu-id="48a3d-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="48a3d-120">O único tipo com suporte é MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="48a3d-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="48a3d-121">_ulStateMask_: O único estado com suporte é MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="48a3d-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48a3d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="48a3d-122">See also</span></span>

- [<span data-ttu-id="48a3d-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="48a3d-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="48a3d-124">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="48a3d-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="48a3d-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="48a3d-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="48a3d-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="48a3d-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

