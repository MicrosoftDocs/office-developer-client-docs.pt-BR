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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766982"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="20acd-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="20acd-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="20acd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20acd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20acd-105">Obtém o status associado a uma mensagem em uma pasta particular (por exemplo, se a mensagem é marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="20acd-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="20acd-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="20acd-106">Parameters</span></span>

 <span data-ttu-id="20acd-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="20acd-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="20acd-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="20acd-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="20acd-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="20acd-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="20acd-110">[in] Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.</span><span class="sxs-lookup"><span data-stu-id="20acd-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="20acd-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20acd-111">_ulFlags_</span></span>
  
> <span data-ttu-id="20acd-112">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="20acd-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="20acd-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="20acd-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="20acd-114">[out] Um ponteiro para um ponteiro para uma bitmask dos sinalizadores que indicam o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="20acd-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="20acd-115">Bits de 0 a 15 são reservados e devem ser zero; bits 16 a 31 estarão disponíveis para uso específico de implementação.</span><span class="sxs-lookup"><span data-stu-id="20acd-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="20acd-116">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="20acd-116">The following flags can be set:</span></span>
    
<span data-ttu-id="20acd-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="20acd-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="20acd-118">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="20acd-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="20acd-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="20acd-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="20acd-120">A mensagem não será exibido.</span><span class="sxs-lookup"><span data-stu-id="20acd-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="20acd-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="20acd-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="20acd-122">A mensagem deve ser exibida realçado.</span><span class="sxs-lookup"><span data-stu-id="20acd-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="20acd-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="20acd-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="20acd-124">A mensagem foi marcada para exclusão na loja remota de mensagens sem baixar no cliente local.</span><span class="sxs-lookup"><span data-stu-id="20acd-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="20acd-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="20acd-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="20acd-126">A mensagem foi marcada para download a partir do armazenamento de mensagens remoto no cliente local.</span><span class="sxs-lookup"><span data-stu-id="20acd-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="20acd-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="20acd-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="20acd-128">A mensagem foram marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="20acd-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20acd-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="20acd-129">Return value</span></span>

<span data-ttu-id="20acd-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="20acd-130">S_OK</span></span> 
  
> <span data-ttu-id="20acd-131">O status da mensagem foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="20acd-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20acd-132">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="20acd-132">Remarks</span></span>

<span data-ttu-id="20acd-133">O método **IMAPIFolder::GetMessageStatus** retorna o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="20acd-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="20acd-134">Status da mensagem é armazenado na propriedade de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="20acd-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20acd-135">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="20acd-135">Notes to implementers</span></span>

<span data-ttu-id="20acd-136">Como os bits de status da mensagem estiver definidos, desmarcados e usados dependem completamente a implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="20acd-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="20acd-137">Se você armazenar mensagens na subárvore IPM, MAPI reserva bits 16 a 31 para uso por clientes IPM.</span><span class="sxs-lookup"><span data-stu-id="20acd-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="20acd-138">Se você armazenar mensagens em outros subárvores, você pode usar o bits 16 a 31 para fins de seus próprios.</span><span class="sxs-lookup"><span data-stu-id="20acd-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="20acd-139">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="20acd-139">MFCMAPI reference</span></span>

<span data-ttu-id="20acd-140">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="20acd-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="20acd-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="20acd-141">**File**</span></span>|<span data-ttu-id="20acd-142">**Function**</span><span class="sxs-lookup"><span data-stu-id="20acd-142">**Function**</span></span>|<span data-ttu-id="20acd-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="20acd-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20acd-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="20acd-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="20acd-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="20acd-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="20acd-146">MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem próximo a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="20acd-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="20acd-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="20acd-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="20acd-148">OpenMessageNonModal e OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="20acd-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="20acd-149">MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem a ser exibido para passar para a tela de formulário, que é CMyMAPIFormViewer ou [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="20acd-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20acd-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="20acd-150">See also</span></span>



[<span data-ttu-id="20acd-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="20acd-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="20acd-152">IMAPISession:: ShowForm</span><span class="sxs-lookup"><span data-stu-id="20acd-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="20acd-153">Propriedade canônico de PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="20acd-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="20acd-154">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="20acd-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="20acd-155">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="20acd-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

