---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418635"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="b8b39-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b8b39-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="b8b39-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8b39-105">Obtém o status associado a uma mensagem em uma pasta específica (por exemplo, se essa mensagem está marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="b8b39-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="b8b39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8b39-106">Parameters</span></span>

 <span data-ttu-id="b8b39-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8b39-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b8b39-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="b8b39-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b8b39-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8b39-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b8b39-110">[in] Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.</span><span class="sxs-lookup"><span data-stu-id="b8b39-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="b8b39-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8b39-111">_ulFlags_</span></span>
  
> <span data-ttu-id="b8b39-112">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8b39-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b8b39-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="b8b39-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="b8b39-114">[out] Um ponteiro para um ponteiro para uma máscara de bits de sinalizadores que indicam o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8b39-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="b8b39-115">Os bits de 0 a 15 são reservados e devem ser zero; os bits 16 a 31 estão disponíveis para uso específico da implementação.</span><span class="sxs-lookup"><span data-stu-id="b8b39-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="b8b39-116">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b8b39-116">The following flags can be set:</span></span>
    
<span data-ttu-id="b8b39-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="b8b39-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="b8b39-118">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="b8b39-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="b8b39-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="b8b39-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="b8b39-120">A mensagem não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="b8b39-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="b8b39-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="b8b39-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="b8b39-122">A mensagem deve ser exibida realçada.</span><span class="sxs-lookup"><span data-stu-id="b8b39-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="b8b39-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="b8b39-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="b8b39-124">A mensagem foi marcada para exclusão no armazenamento de mensagens remoto sem ser baixada para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="b8b39-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="b8b39-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="b8b39-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="b8b39-126">A mensagem foi marcada para download do armazenamento de mensagens remoto para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="b8b39-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="b8b39-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="b8b39-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="b8b39-128">A mensagem foi marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="b8b39-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8b39-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8b39-129">Return value</span></span>

<span data-ttu-id="b8b39-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8b39-130">S_OK</span></span> 
  
> <span data-ttu-id="b8b39-131">O status da mensagem foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b8b39-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8b39-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8b39-132">Remarks</span></span>

<span data-ttu-id="b8b39-133">O **método IMAPIFolder::GetMessageStatus** retorna o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8b39-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="b8b39-134">O status da mensagem é armazenado na propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8b39-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b8b39-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b8b39-135">Notes to implementers</span></span>

<span data-ttu-id="b8b39-136">A maneira como os bits de status da mensagem são definidos, limpos e usados depende completamente da implementação, exceto pelo fato de que os bits de 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8b39-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="b8b39-137">Se você armazenar mensagens na subárvore do IPM, o MAPI reserva bits de 16 a 31 para uso por clientes IPM.</span><span class="sxs-lookup"><span data-stu-id="b8b39-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="b8b39-138">Se você armazenar mensagens em outras subárvore, poderá usar os bits 16 a 31 para suas próprias finalidades.</span><span class="sxs-lookup"><span data-stu-id="b8b39-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8b39-139">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8b39-139">MFCMAPI reference</span></span>

<span data-ttu-id="b8b39-140">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8b39-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8b39-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b8b39-141">**File**</span></span>|<span data-ttu-id="b8b39-142">**Função**</span><span class="sxs-lookup"><span data-stu-id="b8b39-142">**Function**</span></span>|<span data-ttu-id="b8b39-143">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b8b39-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8b39-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b8b39-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b8b39-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="b8b39-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="b8b39-146">MFCMAPI usa o **método IMAPIFolder::GetMessageStatus** para obter o status da próxima mensagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="b8b39-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="b8b39-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b8b39-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b8b39-148">OpenMessageNonModal e OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="b8b39-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="b8b39-149">MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem a ser exibida para passar para o visualizador de formulário, que é CMyMAPIFormViewer ou [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="b8b39-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8b39-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8b39-150">See also</span></span>



[<span data-ttu-id="b8b39-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b8b39-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="b8b39-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="b8b39-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="b8b39-153">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b8b39-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="b8b39-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b8b39-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="b8b39-155">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b8b39-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

