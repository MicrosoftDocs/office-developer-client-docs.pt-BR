---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: beeca6ba958c38e12fba7dbc2884c81e58bdf3c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590117"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="51574-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="51574-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="51574-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51574-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51574-105">Registra um coletor advise para receber notificações por meio de MAPI.</span><span class="sxs-lookup"><span data-stu-id="51574-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="51574-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51574-106">Parameters</span></span>

 <span data-ttu-id="51574-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="51574-107">_lpKey_</span></span>
  
> <span data-ttu-id="51574-108">[in] Um ponteiro para uma chave de notificação que representa o objeto de origem advise.</span><span class="sxs-lookup"><span data-stu-id="51574-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="51574-109">O parâmetro _lpKey_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="51574-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="51574-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="51574-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="51574-111">[in] Uma máscara de valores que indicam os tipos de eventos de notificação que o chamador está interessado em e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="51574-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="51574-112">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="51574-112">The following values are valid:</span></span>
    
 <span data-ttu-id="51574-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="51574-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="51574-114">Registradores para notificações sobre erros graves, como as de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="51574-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="51574-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="51574-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="51574-116">Provedor de armazenamento de registradores para notificações sobre eventos específicos ao catálogo de endereços particular ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="51574-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="51574-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="51574-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="51574-118">Registradores para notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="51574-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="51574-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="51574-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="51574-120">Registradores para notificações sobre a criação de um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="51574-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="51574-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="51574-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="51574-122">Registradores para notificações sobre um objeto que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="51574-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="51574-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="51574-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="51574-124">Registradores para notificações sobre um objeto que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="51574-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="51574-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="51574-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="51574-126">Registradores para notificações sobre um objeto que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="51574-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="51574-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="51574-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="51574-128">Registradores para notificações sobre um objeto que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="51574-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="51574-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="51574-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="51574-130">Registradores para notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="51574-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="51574-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51574-131">_ulFlags_</span></span>
  
> <span data-ttu-id="51574-132">[in] Uma bitmask dos sinalizadores que controla como ocorre a notificação.</span><span class="sxs-lookup"><span data-stu-id="51574-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="51574-133">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="51574-133">The following flag can be set:</span></span>
    
<span data-ttu-id="51574-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="51574-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="51574-135">Quando o chamador chama o método [IMAPISupport::Notify](imapisupport-notify.md) para gerar notificações para esse coletor advise, **Notify** deve fazer todas as chamadas necessárias aos receptores de aviso antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="51574-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="51574-136">Se esse sinalizador não estiver definida, notificação é assíncrona e retornos de chamada são enfileirados aos processos que tem se inscrito e iniciado quando esses processos assumir o controle da CPU.</span><span class="sxs-lookup"><span data-stu-id="51574-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="51574-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="51574-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="51574-138">[in] Um ponteiro para um objeto de coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="51574-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="51574-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="51574-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="51574-140">[out] Um ponteiro para um número diferente de zero de conexão que representa o registro.</span><span class="sxs-lookup"><span data-stu-id="51574-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51574-141">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="51574-141">Return value</span></span>

<span data-ttu-id="51574-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="51574-142">S_OK</span></span> 
  
> <span data-ttu-id="51574-143">O registro de notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="51574-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51574-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="51574-144">Remarks</span></span>

<span data-ttu-id="51574-145">O método **IMAPISupport::Subscribe** é implementado para todos os objetos de suporte de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="51574-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="51574-146">Provedores de serviços chamarem **Subscribe** de um dos seus métodos **Advise** para permitir que o MAPI gerenciar as notificações.</span><span class="sxs-lookup"><span data-stu-id="51574-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51574-147">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="51574-147">Notes to callers</span></span>

<span data-ttu-id="51574-148">Para usar os métodos de suporte MAPI para fins de notificação, crie uma chave para a fonte de advise o objeto sobre o qual as notificações deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="51574-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="51574-149">O valor da chave deve ser exclusivo e deve ser facilmente gerar toda vez que o objeto altera.</span><span class="sxs-lookup"><span data-stu-id="51574-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="51574-150">MAPI usa a chave de notificação para procurar qualquer funções de retorno de chamada registradas por meio da função [HrAllocAdviseSink](hrallocadvisesink.md) para a fonte de advise correspondente.</span><span class="sxs-lookup"><span data-stu-id="51574-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="51574-151">Passe essa chave para **IMAPISupport::Notify** sempre que precisar gerar uma notificação para a fonte de advise correspondente.</span><span class="sxs-lookup"><span data-stu-id="51574-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="51574-152">O sinalizador NOTIFY_SYNC afeta a operação de chamadas subsequentes para **Notificar**.</span><span class="sxs-lookup"><span data-stu-id="51574-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="51574-153">Quando você define NOTIFY_SYNC, **Notify** não retorna até que ele tenha terminado enviar todas as notificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="51574-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="51574-154">Quando você não definir NOTIFY_SYNC, **Notify** opera de forma assíncrona, retornando possivelmente antes de todas as notificações foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="51574-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51574-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="51574-155">See also</span></span>



[<span data-ttu-id="51574-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="51574-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="51574-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="51574-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="51574-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="51574-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="51574-159">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="51574-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="51574-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="51574-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="51574-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="51574-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

