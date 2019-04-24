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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348745"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="fa976-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="fa976-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="fa976-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa976-105">Bloqueia ou desbloqueia uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="fa976-105">Locks or unlocks a message.</span></span> <span data-ttu-id="fa976-106">Este método é chamado apenas pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa976-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="fa976-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa976-107">Parameters</span></span>

 <span data-ttu-id="fa976-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="fa976-108">_lpMessage_</span></span>
  
> <span data-ttu-id="fa976-109">no Um ponteiro para a mensagem a ser bloqueada ou desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="fa976-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="fa976-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="fa976-110">_ulLockState_</span></span>
  
> <span data-ttu-id="fa976-111">no Um valor que indica se a mensagem deve ser bloqueada ou desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="fa976-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="fa976-112">Um dos seguintes valores é válido:</span><span class="sxs-lookup"><span data-stu-id="fa976-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="fa976-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="fa976-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="fa976-114">A mensagem deve ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="fa976-114">The message should be locked.</span></span> 
    
<span data-ttu-id="fa976-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="fa976-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="fa976-116">A mensagem deve ser desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="fa976-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa976-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fa976-117">Return value</span></span>

<span data-ttu-id="fa976-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa976-118">S_OK</span></span> 
  
> <span data-ttu-id="fa976-119">O estado de bloqueio da mensagem foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="fa976-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa976-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa976-120">Remarks</span></span>

<span data-ttu-id="fa976-121">O método **IMsgStore::** setlockstate bloqueia ou desbloqueia uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="fa976-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="fa976-122">\*\*\*\* Setlockstate só pode ser chamado pelo spooler MAPI enquanto ele está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="fa976-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="fa976-123">Normalmente, quando o spooler MAPI chama setLockstate para bloquear uma mensagem, ele bloqueia somente a mensagem mais antiga (ou seja, a próxima mensagem enfileirada para o spooler MAPI a ser enviado). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="fa976-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="fa976-124">Se a mensagem mais antiga na fila estiver aguardando um provedor de transporte temporariamente indisponível e a próxima mensagem na fila usar um provedor de transporte diferente, o spooler MAPI poderá começar a processar a mensagem mais tarde.</span><span class="sxs-lookup"><span data-stu-id="fa976-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="fa976-125">Ele começa o processamento bloqueando essa mensagem usando \*\*\*\* setlockstate.</span><span class="sxs-lookup"><span data-stu-id="fa976-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fa976-126">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="fa976-126">Notes to implementers</span></span>

<span data-ttu-id="fa976-127">Após o spooler MAPI ter chamado setLockstate com o parâmetro _ulLockState_ definido como MSG_LOCKED, as chamadas para o método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para cancelar a transmissão da mensagem devem falhar. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="fa976-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="fa976-128">Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem em sua \*\*\*\* implementação setlockstate para que quaisquer alterações feitas à mensagem antes da chamada setlockstate sejam salvas. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="fa976-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa976-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa976-129">See also</span></span>



[<span data-ttu-id="fa976-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="fa976-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="fa976-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="fa976-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="fa976-132">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fa976-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

