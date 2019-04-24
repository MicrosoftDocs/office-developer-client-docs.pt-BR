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
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334472"
---
# <a name="notifcallback"></a><span data-ttu-id="6997d-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="6997d-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="6997d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6997d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6997d-105">Define uma função de retorno de chamada que MAPI chama para enviar uma notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="6997d-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="6997d-106">Essa função de retorno de chamada só pode ser usada quando empacotado em um objeto de coletor de aviso criado chamando-se a função [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="6997d-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6997d-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6997d-107">Header file:</span></span>  <br/> |<span data-ttu-id="6997d-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6997d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6997d-109">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="6997d-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="6997d-110">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6997d-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="6997d-111">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="6997d-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="6997d-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="6997d-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="6997d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6997d-113">Parameters</span></span>

 <span data-ttu-id="6997d-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="6997d-114">_lpvContext_</span></span>
  
> <span data-ttu-id="6997d-115">no Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama.</span><span class="sxs-lookup"><span data-stu-id="6997d-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="6997d-116">Esse valor pode representar um endereço de importância para o aplicativo cliente ou provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6997d-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="6997d-117">Normalmente, para o código C++, o parâmetro _lpvContext_ representa um ponteiro para um objeto C++.</span><span class="sxs-lookup"><span data-stu-id="6997d-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="6997d-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="6997d-118">_cNotification_</span></span>
  
> <span data-ttu-id="6997d-119">no Contagem de notificações de eventos na matriz indicada pelo parâmetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="6997d-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="6997d-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="6997d-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="6997d-121">bota Ponteiro para o local onde essa função grava uma matriz de estruturas de [notificação](notification.md) que contém as notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="6997d-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6997d-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6997d-122">Return value</span></span>

<span data-ttu-id="6997d-123">O conjunto de valores de retorno válidos para o protótipo de função **NOTIFCALLBACK** depende se a função é implementada por um aplicativo cliente ou um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6997d-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="6997d-124">Os clientes sempre devem retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="6997d-124">Clients should always return S_OK.</span></span> <span data-ttu-id="6997d-125">Os provedores podem retornar S_OK ou CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="6997d-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6997d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="6997d-126">Remarks</span></span>

<span data-ttu-id="6997d-127">CALLBACK_DISCONTINUE é um valor de retorno válido apenas para funções de retorno de chamada síncronas; Ele solicita que MAPI imediatamente pare de processar os retornos de chamada para esta notificação.</span><span class="sxs-lookup"><span data-stu-id="6997d-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="6997d-128">Quando CALLBACK_DISCONTINUE é retornado, MAPI define o parâmetro _lpUlFlags_ como NOTIFY_CANCELED quando retorna de [IMAPISupport:: Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="6997d-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="6997d-129">Veja a seguir limitações sobre o que uma função de retorno de chamada síncrona pode fazer:</span><span class="sxs-lookup"><span data-stu-id="6997d-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="6997d-130">Não é possível fazer com que outra notificação síncrona seja gerada.</span><span class="sxs-lookup"><span data-stu-id="6997d-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="6997d-131">Não é possível exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6997d-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6997d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6997d-132">See also</span></span>



[<span data-ttu-id="6997d-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6997d-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

