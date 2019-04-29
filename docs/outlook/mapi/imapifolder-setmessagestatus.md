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
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="60eea-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="60eea-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="60eea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60eea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60eea-105">Define o status associado a uma mensagem (por exemplo, se a mensagem está marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="60eea-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="60eea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60eea-106">Parameters</span></span>

 <span data-ttu-id="60eea-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="60eea-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="60eea-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="60eea-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="60eea-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="60eea-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="60eea-110">no Um ponteiro para o identificador de entrada da mensagem cujo status é definido.</span><span class="sxs-lookup"><span data-stu-id="60eea-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="60eea-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="60eea-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="60eea-112">no O novo status a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="60eea-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="60eea-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="60eea-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="60eea-114">no Uma bitmask de sinalizadores que é aplicada ao novo status e indica os sinalizadores a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="60eea-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="60eea-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="60eea-115">The following flags can be set:</span></span>
    
<span data-ttu-id="60eea-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="60eea-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="60eea-117">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="60eea-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="60eea-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="60eea-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="60eea-119">A mensagem não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="60eea-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="60eea-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="60eea-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="60eea-121">A mensagem deve ser exibida em destaque.</span><span class="sxs-lookup"><span data-stu-id="60eea-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="60eea-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="60eea-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="60eea-123">A mensagem foi marcada para exclusão no armazenamento remoto de mensagens sem baixar para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="60eea-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="60eea-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="60eea-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="60eea-125">A mensagem foi marcada para download no repositório de mensagens remotas para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="60eea-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="60eea-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="60eea-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="60eea-127">A mensagem foi marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="60eea-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="60eea-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="60eea-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="60eea-129">bota Um ponteiro para o status anterior da mensagem.</span><span class="sxs-lookup"><span data-stu-id="60eea-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60eea-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="60eea-130">Return value</span></span>

<span data-ttu-id="60eea-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="60eea-131">S_OK</span></span> 
  
> <span data-ttu-id="60eea-132">O status da mensagem foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="60eea-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60eea-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="60eea-133">Remarks</span></span>

<span data-ttu-id="60eea-134">O método **IMAPIFolder:: SetMessageStatus** define o status da mensagem para o valor armazenado na sua propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="60eea-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="60eea-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="60eea-135">Notes to implementers</span></span>

<span data-ttu-id="60eea-136">Como os bits de status de mensagem são definidos, limpos e usados dependem completamente da sua implementação, exceto pelo fato de que os bits 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="60eea-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="60eea-137">A implementação de um provedor de transporte remoto desse método deve seguir as semânticas descritas aqui.</span><span class="sxs-lookup"><span data-stu-id="60eea-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="60eea-138">Não há considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="60eea-138">There are no special considerations.</span></span> <span data-ttu-id="60eea-139">Os clientes usam esse método para definir os bits MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE para indicar que uma determinada mensagem deve ser baixada ou excluída do repositório de mensagens remoto.</span><span class="sxs-lookup"><span data-stu-id="60eea-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="60eea-140">Um provedor de transporte remoto não precisa implementar o método [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) relacionado.</span><span class="sxs-lookup"><span data-stu-id="60eea-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="60eea-141">Os clientes devem procurar na tabela de conteúdo da pasta para determinar o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="60eea-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="60eea-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="60eea-142">Notes to callers</span></span>

<span data-ttu-id="60eea-143">Você pode usar a propriedade **PR_MSG_STATUS** de uma mensagem para negociar uma operação de bloqueio de mensagens com outros clientes.</span><span class="sxs-lookup"><span data-stu-id="60eea-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="60eea-144">Designar um bit como o bit de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="60eea-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="60eea-145">Para determinar se o bit de bloqueio foi definido, examine o valor anterior para status da mensagem no parâmetro _lpulOldStatus_ .</span><span class="sxs-lookup"><span data-stu-id="60eea-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="60eea-146">Use os outros bits no parâmetro _ulNewStatus_ para rastrear o status da mensagem sem interferir no bit de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="60eea-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60eea-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="60eea-147">See also</span></span>



[<span data-ttu-id="60eea-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="60eea-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="60eea-149">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="60eea-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="60eea-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="60eea-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

