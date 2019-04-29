---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435933"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="0d997-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="0d997-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="0d997-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d997-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d997-105">Envia uma notificação de um evento especificado para uma fonte de aviso registrada originalmente para a notificação por meio do método [IMAPISupport:: Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="0d997-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0d997-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d997-106">Parameters</span></span>

<span data-ttu-id="0d997-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="0d997-107">_lpKey_</span></span>
  
> <span data-ttu-id="0d997-108">no Um ponteiro para a chave de notificação para o objeto de origem de aviso.</span><span class="sxs-lookup"><span data-stu-id="0d997-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="0d997-109">O parâmetro _lpKey_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="0d997-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="0d997-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="0d997-110">_cNotification_</span></span>
  
> <span data-ttu-id="0d997-111">no A contagem de estruturas de notificação apontadas pelo parâmetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="0d997-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="0d997-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="0d997-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="0d997-113">no Um ponteiro para uma matriz de estruturas de [notificação](notification.md) que descrevem as notificações pendentes.</span><span class="sxs-lookup"><span data-stu-id="0d997-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="0d997-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d997-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="0d997-115">[in, out] Uma bitmask de sinalizadores que controlam o processo de notificação.</span><span class="sxs-lookup"><span data-stu-id="0d997-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="0d997-116">Na entrada, o seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="0d997-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="0d997-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d997-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="0d997-118">As cadeias de caracteres nas estruturas de notificação apontadas pelo _lpNotifications_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0d997-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="0d997-119">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0d997-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="0d997-120">Na saída, o MAPI pode definir o seguinte sinalizador:</span><span class="sxs-lookup"><span data-stu-id="0d997-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="0d997-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="0d997-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="0d997-122">Uma função de retorno de chamada cancelou uma notificação síncrona.</span><span class="sxs-lookup"><span data-stu-id="0d997-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d997-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d997-123">Return value</span></span>

<span data-ttu-id="0d997-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d997-124">S_OK</span></span> 
  
> <span data-ttu-id="0d997-125">As notificações foram geradas com êxito.</span><span class="sxs-lookup"><span data-stu-id="0d997-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d997-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d997-126">Remarks</span></span>

<span data-ttu-id="0d997-127">O método **IMAPISupport:: Notify** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="0d997-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="0d997-128">Os provedores de \*\*\*\* serviços de chamadas notificam para solicitar que o MAPI gere uma notificação para um coletor de aviso registrado anteriormente para a notificação através do método **IMAPISupport:: Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="0d997-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="0d997-129">**Notify** copia as estruturas apontadas pelo parâmetro _lpNotifications_ para a memória e chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de avisos apropriado.</span><span class="sxs-lookup"><span data-stu-id="0d997-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="0d997-130">Quando **OnNotify** é concluído com a notificação, ele libera a memória envolvida.</span><span class="sxs-lookup"><span data-stu-id="0d997-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="0d997-131">O chamador não precisa alocar memória; O MAPI realiza todas as alocações de memória necessárias.</span><span class="sxs-lookup"><span data-stu-id="0d997-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0d997-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0d997-132">Notes to callers</span></span>

<span data-ttu-id="0d997-133">A chave de notificação passada no parâmetro _lpKey_ deve ser idêntica à chave passada em _lpKey_ para o método **IMAPISupport:: Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="0d997-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="0d997-134">Muitos provedores usam o identificador de entrada da fonte de aviso como a chave, mas outros dados, como um caminho de arquivo, podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="0d997-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="0d997-135">O MAPI usa essa chave para localizar todos os registros de notificações na fonte de aviso identificada.</span><span class="sxs-lookup"><span data-stu-id="0d997-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="0d997-136">Certifique-se de definir o membro **lpEntryID** da estrutura de notificação para um identificador de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="0d997-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="0d997-137">Se você definir o sinalizador NOTIFY_SYNC na chamada **Subscribe** para qualquer uma das notificações pendentes, **notifique** as chamadas as funções de retorno de chamada do método **IMAPIAdviseSink:: OnNotify** antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="0d997-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="0d997-138">Um coletor de aviso pode ser criado manualmente ou chamando [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="0d997-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="0d997-139">A função **HrAllocAdviseSink** permite que o chamador especifique uma função de retorno de chamada que **notifique** as chamadas como parte da notificação.</span><span class="sxs-lookup"><span data-stu-id="0d997-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="0d997-140">A função de retorno de chamada está em conformidade com o protótipo [NOTIFCALLBACK](notifcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="0d997-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="0d997-141">As funções de retorno de chamada implementadas por clientes sempre retornam S_OK; as funções de retorno de chamada implementadas por provedores de serviços podem retornar CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="0d997-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="0d997-142">Se uma função de retorno de chamada retornar CALLBACK_DISCONTINUE, o MAPI interromperá o envio de notificações e retornará NOTIFY_CANCELED no parâmetro _lpulFlags_ do método **Notify** .</span><span class="sxs-lookup"><span data-stu-id="0d997-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="0d997-143">Você pode supor que o processo está inativo e parar de gerar notificações para esse processo.</span><span class="sxs-lookup"><span data-stu-id="0d997-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="0d997-144">Se **notificar** retornar 0 no _lpulFlags_, o processo ainda estará ativo e você deverá continuar a enviar notificações, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="0d997-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="0d997-145">Ao usar notificações síncronas, tenha cuidado para evitar situações de deadlock.</span><span class="sxs-lookup"><span data-stu-id="0d997-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="0d997-146">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0d997-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d997-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d997-147">See also</span></span>

- [<span data-ttu-id="0d997-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="0d997-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="0d997-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="0d997-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="0d997-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="0d997-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="0d997-151">Notifica</span><span class="sxs-lookup"><span data-stu-id="0d997-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="0d997-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="0d997-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="0d997-153">Propriedade canônica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="0d997-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="0d997-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d997-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

