---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768156"
---
# <a name="notifcallback"></a><span data-ttu-id="8af6e-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="8af6e-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="8af6e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8af6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8af6e-105">Define uma função de retorno de chamada que chamadas MAPI para enviar uma notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="8af6e-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="8af6e-106">Essa função de retorno de chamada pode ser usada apenas quando disposto em um objeto de coletor de eventos advise criado chamando-se a função [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="8af6e-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8af6e-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8af6e-107">Header file:</span></span>  <br/> |<span data-ttu-id="8af6e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8af6e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8af6e-109">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="8af6e-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="8af6e-110">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="8af6e-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="8af6e-111">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="8af6e-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="8af6e-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="8af6e-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="8af6e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8af6e-113">Parameters</span></span>

 <span data-ttu-id="8af6e-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="8af6e-114">_lpvContext_</span></span>
  
> <span data-ttu-id="8af6e-115">[in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando chamadas de MAPI-lo.</span><span class="sxs-lookup"><span data-stu-id="8af6e-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="8af6e-116">Esse valor pode representar um endereço de significância para o aplicativo cliente ou o provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="8af6e-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="8af6e-117">Geralmente, para código C++, o parâmetro _lpvContext_ representa um ponteiro para um objeto C++.</span><span class="sxs-lookup"><span data-stu-id="8af6e-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="8af6e-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="8af6e-118">_cNotification_</span></span>
  
> <span data-ttu-id="8af6e-119">[in] Contagem de notificações de evento na matriz indicado pelo parâmetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="8af6e-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="8af6e-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="8af6e-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="8af6e-121">[out] Ponteiro para o local onde essa função grava uma matriz de estruturas de [notificação](notification.md) que contém as notificações de evento.</span><span class="sxs-lookup"><span data-stu-id="8af6e-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8af6e-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8af6e-122">Return value</span></span>

<span data-ttu-id="8af6e-123">O conjunto de valores de retorno válidos para o protótipo de função **NOTIFCALLBACK** depende se a função é implementada por um provedor de serviços ou de um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="8af6e-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="8af6e-124">Clientes sempre devem retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="8af6e-124">Clients should always return S_OK.</span></span> <span data-ttu-id="8af6e-125">Provedores podem retornar S_OK ou CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="8af6e-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8af6e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8af6e-126">Remarks</span></span>

<span data-ttu-id="8af6e-127">CALLBACK_DISCONTINUE é um valor de retorno válido para funções de retorno de chamada síncrona apenas; ele solicita que o MAPI parar imediatamente os retornos de chamada para essa notificação de processamento.</span><span class="sxs-lookup"><span data-stu-id="8af6e-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="8af6e-128">Quando CALLBACK_DISCONTINUE é retornado, MAPI define o parâmetro _lpUlFlags_ para NOTIFY_CANCELED quando ele retorna da [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="8af6e-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="8af6e-129">A seguir estão limitações no que pode fazer uma função de retorno de chamada síncrona:</span><span class="sxs-lookup"><span data-stu-id="8af6e-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="8af6e-130">Ele não pode causar outra notificação síncrona a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="8af6e-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="8af6e-131">Ele não pode exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8af6e-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8af6e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8af6e-132">See also</span></span>



[<span data-ttu-id="8af6e-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8af6e-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

