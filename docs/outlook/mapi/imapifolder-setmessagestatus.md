---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d06523625a20760faec7a6c73a6beaef757818b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575074"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="0ff3d-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0ff3d-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="0ff3d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ff3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ff3d-105">Define o status associado a uma mensagem (por exemplo, se a mensagem é marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="0ff3d-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="0ff3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff3d-106">Parameters</span></span>

 <span data-ttu-id="0ff3d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0ff3d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0ff3d-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="0ff3d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0ff3d-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0ff3d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0ff3d-110">[in] Um ponteiro para o identificador de entrada da mensagem cujo status esteja definido.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="0ff3d-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="0ff3d-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="0ff3d-112">[in] O novo status a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="0ff3d-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="0ff3d-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="0ff3d-114">[in] Uma bitmask dos sinalizadores que é aplicada para o novo status e indica os sinalizadores a ser definido.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="0ff3d-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0ff3d-115">The following flags can be set:</span></span>
    
<span data-ttu-id="0ff3d-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="0ff3d-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="0ff3d-117">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="0ff3d-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="0ff3d-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="0ff3d-119">A mensagem não será exibido.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="0ff3d-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="0ff3d-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="0ff3d-121">A mensagem deve ser exibida realçado.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="0ff3d-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="0ff3d-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="0ff3d-123">A mensagem foi marcada para exclusão na loja remota de mensagens sem baixar no cliente local.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="0ff3d-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="0ff3d-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="0ff3d-125">A mensagem foi marcada para download a partir do armazenamento de mensagens remoto no cliente local.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="0ff3d-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="0ff3d-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="0ff3d-127">A mensagem foram marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="0ff3d-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="0ff3d-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="0ff3d-129">[out] Um ponteiro para o status anterior da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ff3d-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0ff3d-130">Return value</span></span>

<span data-ttu-id="0ff3d-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ff3d-131">S_OK</span></span> 
  
> <span data-ttu-id="0ff3d-132">O status da mensagem foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ff3d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ff3d-133">Remarks</span></span>

<span data-ttu-id="0ff3d-134">O método **IMAPIFolder::SetMessageStatus** define o status da mensagem com o valor armazenado na sua propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0ff3d-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0ff3d-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="0ff3d-135">Notes to implementers</span></span>

<span data-ttu-id="0ff3d-136">Como os bits de status da mensagem estiver definidos, desmarcados e usados dependem completamente a implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="0ff3d-137">Implementação de um provedor de transporte remoto deste método deve seguir a semântica descrita aqui.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="0ff3d-138">Não há nenhuma considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-138">There are no special considerations.</span></span> <span data-ttu-id="0ff3d-139">Clientes usam esse método para definir os bits MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE para indicar que uma mensagem específica é a serem baixadas ou excluído do armazenamento remoto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="0ff3d-140">Não tem um provedor de transporte remoto implementar o método [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) relacionado.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="0ff3d-141">Os clientes devem procure na tabela de conteúdo da pasta para determinar o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0ff3d-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0ff3d-142">Notes to callers</span></span>

<span data-ttu-id="0ff3d-143">Você pode usar a propriedade **PR_MSG_STATUS** de uma mensagem para negociar uma operação de bloqueio de mensagem com outros clientes.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="0ff3d-144">Designe um pouco como o bit de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="0ff3d-145">Para determinar se foi definido o bit de bloqueio, examine o valor anterior para o status da mensagem no parâmetro _lpulOldStatus_ .</span><span class="sxs-lookup"><span data-stu-id="0ff3d-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="0ff3d-146">Use os outros bits no parâmetro _ulNewStatus_ para acompanhar o status da mensagem sem interferir estará definido o bit bloqueio.</span><span class="sxs-lookup"><span data-stu-id="0ff3d-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ff3d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ff3d-147">See also</span></span>



[<span data-ttu-id="0ff3d-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0ff3d-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="0ff3d-149">Propriedade canônico de PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0ff3d-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="0ff3d-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0ff3d-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

