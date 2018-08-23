---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2efee531e277b6295b7d4bc299eefc789a805d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571084"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="deef2-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="deef2-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="deef2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deef2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deef2-105">Bloqueia ou desbloqueia uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="deef2-105">Locks or unlocks a message.</span></span> <span data-ttu-id="deef2-106">Este método é chamado somente pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="deef2-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="deef2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deef2-107">Parameters</span></span>

 <span data-ttu-id="deef2-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="deef2-108">_lpMessage_</span></span>
  
> <span data-ttu-id="deef2-109">[in] Um ponteiro para a mensagem para bloquear ou desbloquear.</span><span class="sxs-lookup"><span data-stu-id="deef2-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="deef2-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="deef2-110">_ulLockState_</span></span>
  
> <span data-ttu-id="deef2-111">[in] Um valor que indica se a mensagem deve ser bloqueada ou desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="deef2-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="deef2-112">Um dos valores a seguir é válido:</span><span class="sxs-lookup"><span data-stu-id="deef2-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="deef2-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="deef2-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="deef2-114">A mensagem deve ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="deef2-114">The message should be locked.</span></span> 
    
<span data-ttu-id="deef2-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="deef2-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="deef2-116">A mensagem deve ser desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="deef2-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="deef2-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="deef2-117">Return value</span></span>

<span data-ttu-id="deef2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="deef2-118">S_OK</span></span> 
  
> <span data-ttu-id="deef2-119">O estado de bloqueio da mensagem foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="deef2-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="deef2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="deef2-120">Remarks</span></span>

<span data-ttu-id="deef2-121">O método **IMsgStore::SetLockState** bloqueia ou desbloqueia uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="deef2-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="deef2-122">**SetLockState** pode ser chamado apenas pelo spooler MAPI enquanto ele está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="deef2-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="deef2-123">Normalmente, quando o MAPI spooler chama **SetLockState** para bloquear uma mensagem, ele bloqueia somente a mensagem mais antiga (ou seja, a próxima mensagem na fila para o spooler MAPI enviar).</span><span class="sxs-lookup"><span data-stu-id="deef2-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="deef2-124">Se a mensagem mais antiga na fila está aguardando para um provedor de transporte temporariamente indisponível e a próxima mensagem na fila usa um provedor de transporte diferentes, o MAPI spooler pode começar a processar a mensagem posterior.</span><span class="sxs-lookup"><span data-stu-id="deef2-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="deef2-125">Ele começará processamento bloqueando mensagem usando **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="deef2-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="deef2-126">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="deef2-126">Notes to implementers</span></span>

<span data-ttu-id="deef2-127">Depois que o MAPI spooler tiver chamado **SetLockState** com o parâmetro _ulLockState_ definido como MSG_LOCKED, chamadas ao método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para cancelar a transmissão da mensagem devem falhar.</span><span class="sxs-lookup"><span data-stu-id="deef2-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="deef2-128">Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem na sua implementação **SetLockState** para que quaisquer alterações que foram feitas à mensagem antes que a chamada **SetLockState** foi recebida sejam salvas.</span><span class="sxs-lookup"><span data-stu-id="deef2-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="deef2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="deef2-129">See also</span></span>



[<span data-ttu-id="deef2-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="deef2-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="deef2-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="deef2-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="deef2-132">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="deef2-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

