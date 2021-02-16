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
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417270"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="ca608-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ca608-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="ca608-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca608-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca608-105">Define o status associado a uma mensagem (por exemplo, se essa mensagem está marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="ca608-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="ca608-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca608-106">Parameters</span></span>

 <span data-ttu-id="ca608-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca608-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ca608-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ca608-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ca608-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca608-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ca608-110">[in] Um ponteiro para o identificador de entrada da mensagem cujo status está definido.</span><span class="sxs-lookup"><span data-stu-id="ca608-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="ca608-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="ca608-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="ca608-112">[in] O novo status a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="ca608-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="ca608-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="ca608-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="ca608-114">[in] Uma máscara de bits de sinalizadores que é aplicada ao novo status e indica os sinalizadores a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="ca608-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="ca608-115">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ca608-115">The following flags can be set:</span></span>
    
<span data-ttu-id="ca608-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="ca608-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="ca608-117">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="ca608-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="ca608-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="ca608-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="ca608-119">A mensagem não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="ca608-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="ca608-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="ca608-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="ca608-121">A mensagem deve ser exibida realçada.</span><span class="sxs-lookup"><span data-stu-id="ca608-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="ca608-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="ca608-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="ca608-123">A mensagem foi marcada para exclusão no armazenamento de mensagens remoto sem ser baixada para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="ca608-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="ca608-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ca608-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ca608-125">A mensagem foi marcada para download do armazenamento de mensagens remoto para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="ca608-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="ca608-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="ca608-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="ca608-127">A mensagem foi marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ca608-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="ca608-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="ca608-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="ca608-129">[out] Um ponteiro para o status anterior da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca608-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca608-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca608-130">Return value</span></span>

<span data-ttu-id="ca608-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca608-131">S_OK</span></span> 
  
> <span data-ttu-id="ca608-132">O status da mensagem foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="ca608-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca608-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca608-133">Remarks</span></span>

<span data-ttu-id="ca608-134">O **método IMAPIFolder::SetMessageStatus** define o status da mensagem como o valor armazenado em sua **propriedade PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca608-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ca608-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ca608-135">Notes to implementers</span></span>

<span data-ttu-id="ca608-136">A maneira como os bits de status da mensagem são definidos, limpos e usados depende completamente da implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="ca608-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="ca608-137">A implementação desse método de um provedor de transporte remoto deve seguir a semântica descrita aqui.</span><span class="sxs-lookup"><span data-stu-id="ca608-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="ca608-138">Não há considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="ca608-138">There are no special considerations.</span></span> <span data-ttu-id="ca608-139">Os clientes usam esse método para definir os bits MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE bits para indicar que uma mensagem específica deve ser baixada ou excluída do armazenamento de mensagens remoto.</span><span class="sxs-lookup"><span data-stu-id="ca608-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="ca608-140">Um provedor de transporte remoto não precisa implementar o [método IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) relacionado.</span><span class="sxs-lookup"><span data-stu-id="ca608-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="ca608-141">Os clientes devem procurar na tabela de conteúdo da pasta para determinar o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca608-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ca608-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ca608-142">Notes to callers</span></span>

<span data-ttu-id="ca608-143">Você pode usar a **PR_MSG_STATUS** de uma mensagem para negociar uma operação de bloqueio de mensagem com outros clientes.</span><span class="sxs-lookup"><span data-stu-id="ca608-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="ca608-144">Designe um pouco como o bit de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ca608-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="ca608-145">Para determinar se o bit de bloqueio foi definido, examine o valor anterior para o status da mensagem no parâmetro _lpulOldStatus._</span><span class="sxs-lookup"><span data-stu-id="ca608-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="ca608-146">Use os outros bits no  _parâmetro ulNewStatus_ para rastrear o status da mensagem sem interferir no bit de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ca608-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca608-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca608-147">See also</span></span>



[<span data-ttu-id="ca608-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ca608-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="ca608-149">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ca608-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="ca608-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ca608-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

