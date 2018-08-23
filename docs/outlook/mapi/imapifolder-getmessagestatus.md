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
ms.openlocfilehash: 8e5ccadbd6df664b6650487f340508ae4548a1c2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583264"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="78896-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="78896-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="78896-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78896-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78896-105">Obtém o status associado a uma mensagem em uma pasta particular (por exemplo, se a mensagem é marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="78896-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="78896-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78896-106">Parameters</span></span>

 <span data-ttu-id="78896-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="78896-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="78896-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="78896-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="78896-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="78896-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="78896-110">[in] Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.</span><span class="sxs-lookup"><span data-stu-id="78896-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="78896-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78896-111">_ulFlags_</span></span>
  
> <span data-ttu-id="78896-112">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="78896-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="78896-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="78896-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="78896-114">[out] Um ponteiro para um ponteiro para uma bitmask dos sinalizadores que indicam o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="78896-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="78896-115">Bits de 0 a 15 são reservados e devem ser zero; bits 16 a 31 estarão disponíveis para uso específico de implementação.</span><span class="sxs-lookup"><span data-stu-id="78896-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="78896-116">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="78896-116">The following flags can be set:</span></span>
    
<span data-ttu-id="78896-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="78896-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="78896-118">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="78896-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="78896-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="78896-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="78896-120">A mensagem não será exibido.</span><span class="sxs-lookup"><span data-stu-id="78896-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="78896-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="78896-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="78896-122">A mensagem deve ser exibida realçado.</span><span class="sxs-lookup"><span data-stu-id="78896-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="78896-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="78896-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="78896-124">A mensagem foi marcada para exclusão na loja remota de mensagens sem baixar no cliente local.</span><span class="sxs-lookup"><span data-stu-id="78896-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="78896-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="78896-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="78896-126">A mensagem foi marcada para download a partir do armazenamento de mensagens remoto no cliente local.</span><span class="sxs-lookup"><span data-stu-id="78896-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="78896-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="78896-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="78896-128">A mensagem foram marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="78896-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78896-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="78896-129">Return value</span></span>

<span data-ttu-id="78896-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="78896-130">S_OK</span></span> 
  
> <span data-ttu-id="78896-131">O status da mensagem foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="78896-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78896-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="78896-132">Remarks</span></span>

<span data-ttu-id="78896-133">O método **IMAPIFolder::GetMessageStatus** retorna o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="78896-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="78896-134">Status da mensagem é armazenado na propriedade de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="78896-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="78896-135">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="78896-135">Notes to implementers</span></span>

<span data-ttu-id="78896-136">Como os bits de status da mensagem estiver definidos, desmarcados e usados dependem completamente a implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="78896-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="78896-137">Se você armazenar mensagens na subárvore IPM, MAPI reserva bits 16 a 31 para uso por clientes IPM.</span><span class="sxs-lookup"><span data-stu-id="78896-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="78896-138">Se você armazenar mensagens em outros subárvores, você pode usar o bits 16 a 31 para fins de seus próprios.</span><span class="sxs-lookup"><span data-stu-id="78896-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="78896-139">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="78896-139">MFCMAPI reference</span></span>

<span data-ttu-id="78896-140">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="78896-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78896-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="78896-141">**File**</span></span>|<span data-ttu-id="78896-142">**Function**</span><span class="sxs-lookup"><span data-stu-id="78896-142">**Function**</span></span>|<span data-ttu-id="78896-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="78896-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78896-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="78896-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="78896-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="78896-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="78896-146">MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem próximo a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="78896-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="78896-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="78896-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="78896-148">OpenMessageNonModal e OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="78896-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="78896-149">MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem a ser exibido para passar para a tela de formulário, que é CMyMAPIFormViewer ou [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="78896-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78896-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="78896-150">See also</span></span>



[<span data-ttu-id="78896-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="78896-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="78896-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="78896-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="78896-153">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="78896-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="78896-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="78896-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="78896-155">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="78896-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

