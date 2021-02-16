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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419923"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="3ed68-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="3ed68-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="3ed68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ed68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ed68-105">Registra um evento de aviso para receber notificações por meio de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ed68-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3ed68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed68-106">Parameters</span></span>

 <span data-ttu-id="3ed68-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="3ed68-107">_lpKey_</span></span>
  
> <span data-ttu-id="3ed68-108">[in] Um ponteiro para uma chave de notificação que representa o objeto de origem de aviso.</span><span class="sxs-lookup"><span data-stu-id="3ed68-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="3ed68-109">O  _parâmetro lpKey_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="3ed68-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="3ed68-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="3ed68-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="3ed68-111">[in] Uma máscara de valores que indicam os tipos de eventos de notificação nos quais o chamador está interessado e devem ser incluídos no registro.</span><span class="sxs-lookup"><span data-stu-id="3ed68-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="3ed68-112">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="3ed68-112">The following values are valid:</span></span>
    
 <span data-ttu-id="3ed68-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="3ed68-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="3ed68-114">Registra notificações sobre erros graves, como memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="3ed68-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="3ed68-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="3ed68-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="3ed68-116">Registra notificações sobre eventos específicos para o determinado address book ou provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3ed68-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="3ed68-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="3ed68-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="3ed68-118">Registra notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="3ed68-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="3ed68-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="3ed68-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="3ed68-120">Registra notificações sobre a criação de um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="3ed68-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="3ed68-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="3ed68-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="3ed68-122">Registra notificações sobre um objeto sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="3ed68-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="3ed68-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="3ed68-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="3ed68-124">Registra notificações sobre um objeto que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="3ed68-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="3ed68-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="3ed68-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="3ed68-126">Registra notificações sobre um objeto que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="3ed68-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="3ed68-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="3ed68-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="3ed68-128">Registra notificações sobre um objeto que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="3ed68-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="3ed68-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="3ed68-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="3ed68-130">Registra notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3ed68-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="3ed68-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ed68-131">_ulFlags_</span></span>
  
> <span data-ttu-id="3ed68-132">[in] Uma máscara de bits de sinalizadores que controla como a notificação ocorre.</span><span class="sxs-lookup"><span data-stu-id="3ed68-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="3ed68-133">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3ed68-133">The following flag can be set:</span></span>
    
<span data-ttu-id="3ed68-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="3ed68-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="3ed68-135">Quando o chamador chama o método [IMAPISupport::Notify](imapisupport-notify.md) para gerar notificações para esse pia de **aviso,** notificar deve fazer todas as chamadas necessárias para avisar os sinks antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="3ed68-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="3ed68-136">Se esse sinalizador não estiver definido, a notificação será assíncrona e os retornos de chamada serão ensuados para os processos que assinaram e iniciaram quando esses processos ganharem o controle da CPU.</span><span class="sxs-lookup"><span data-stu-id="3ed68-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="3ed68-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="3ed68-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="3ed68-138">[in] Um ponteiro para um objeto de evento de aconselhá-lo.</span><span class="sxs-lookup"><span data-stu-id="3ed68-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="3ed68-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="3ed68-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="3ed68-140">[out] Um ponteiro para um número de conexão que não seja zero que representa o registro.</span><span class="sxs-lookup"><span data-stu-id="3ed68-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ed68-141">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ed68-141">Return value</span></span>

<span data-ttu-id="3ed68-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ed68-142">S_OK</span></span> 
  
> <span data-ttu-id="3ed68-143">O registro de notificação foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3ed68-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ed68-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ed68-144">Remarks</span></span>

<span data-ttu-id="3ed68-145">O **método IMAPISupport::Subscribe** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3ed68-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="3ed68-146">Os provedores de serviços **chamam Subscribe** de um dos métodos **Advise** para permitir que o MAPI gerencie as notificações.</span><span class="sxs-lookup"><span data-stu-id="3ed68-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ed68-147">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3ed68-147">Notes to callers</span></span>

<span data-ttu-id="3ed68-148">Para usar os métodos de suporte MAPI para notificação, crie uma chave para a fonte de avisos sobre o objeto sobre o qual as notificações devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="3ed68-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="3ed68-149">O valor da chave deve ser exclusivo e ser facilmente regenerado sempre que o objeto mudar.</span><span class="sxs-lookup"><span data-stu-id="3ed68-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="3ed68-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span><span class="sxs-lookup"><span data-stu-id="3ed68-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="3ed68-151">Passe essa chave para **IMAPISupport::Notify** sempre que precisar gerar uma notificação para a fonte de aviso correspondente.</span><span class="sxs-lookup"><span data-stu-id="3ed68-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="3ed68-152">O NOTIFY_SYNC sinalizador afeta a operação de chamadas subsequentes para **Notificar.**</span><span class="sxs-lookup"><span data-stu-id="3ed68-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="3ed68-153">Quando você definir NOTIFY_SYNC, o **notify** não retornará até que ele termine de enviar todas as notificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="3ed68-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="3ed68-154">Quando você não definir o NOTIFY_SYNC, o **notify** opera de forma assíncrona, possivelmente retornando antes que todas as notificações tenham sido enviadas.</span><span class="sxs-lookup"><span data-stu-id="3ed68-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ed68-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ed68-155">See also</span></span>



[<span data-ttu-id="3ed68-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3ed68-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="3ed68-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3ed68-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3ed68-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="3ed68-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="3ed68-159">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="3ed68-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="3ed68-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="3ed68-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="3ed68-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ed68-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

