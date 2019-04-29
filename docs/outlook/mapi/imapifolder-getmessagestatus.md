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
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="05cfc-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="05cfc-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="05cfc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05cfc-105">Obtém o status associado a uma mensagem em uma pasta específica (por exemplo, se a mensagem está marcada para exclusão).</span><span class="sxs-lookup"><span data-stu-id="05cfc-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="05cfc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05cfc-106">Parameters</span></span>

 <span data-ttu-id="05cfc-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="05cfc-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="05cfc-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="05cfc-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="05cfc-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="05cfc-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="05cfc-110">no Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.</span><span class="sxs-lookup"><span data-stu-id="05cfc-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="05cfc-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05cfc-111">_ulFlags_</span></span>
  
> <span data-ttu-id="05cfc-112">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="05cfc-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="05cfc-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="05cfc-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="05cfc-114">bota Um ponteiro para um ponteiro para uma bitmask de sinalizadores que indicam o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="05cfc-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="05cfc-115">Os bits de 0 a 15 são reservados e devem ser zero; os bits 16 a 31 estão disponíveis para uso específico da implementação.</span><span class="sxs-lookup"><span data-stu-id="05cfc-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="05cfc-116">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="05cfc-116">The following flags can be set:</span></span>
    
<span data-ttu-id="05cfc-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="05cfc-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="05cfc-118">A mensagem foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="05cfc-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="05cfc-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="05cfc-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="05cfc-120">A mensagem não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="05cfc-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="05cfc-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="05cfc-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="05cfc-122">A mensagem deve ser exibida em destaque.</span><span class="sxs-lookup"><span data-stu-id="05cfc-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="05cfc-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="05cfc-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="05cfc-124">A mensagem foi marcada para exclusão no armazenamento remoto de mensagens sem baixar para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="05cfc-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="05cfc-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="05cfc-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="05cfc-126">A mensagem foi marcada para download no repositório de mensagens remotas para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="05cfc-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="05cfc-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="05cfc-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="05cfc-128">A mensagem foi marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="05cfc-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05cfc-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="05cfc-129">Return value</span></span>

<span data-ttu-id="05cfc-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="05cfc-130">S_OK</span></span> 
  
> <span data-ttu-id="05cfc-131">O status da mensagem foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="05cfc-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05cfc-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="05cfc-132">Remarks</span></span>

<span data-ttu-id="05cfc-133">O método **IMAPIFolder:: GetMessageStatus** retorna o status de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="05cfc-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="05cfc-134">O status da mensagem é armazenado na propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="05cfc-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="05cfc-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="05cfc-135">Notes to implementers</span></span>

<span data-ttu-id="05cfc-136">Como os bits de status de mensagem são definidos, limpos e usados dependem completamente da sua implementação, exceto pelo fato de que os bits 0 a 15 são reservados e devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="05cfc-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="05cfc-137">Se você armazenar mensagens na sub-árvore IPM, o MAPI reserva bits 16 a 31 para uso por clientes IPM.</span><span class="sxs-lookup"><span data-stu-id="05cfc-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="05cfc-138">Se você armazenar mensagens em outras subárvores, poderá usar bits de 16 a 31 para suas próprias finalidades.</span><span class="sxs-lookup"><span data-stu-id="05cfc-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="05cfc-139">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="05cfc-139">MFCMAPI reference</span></span>

<span data-ttu-id="05cfc-140">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="05cfc-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="05cfc-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="05cfc-141">**File**</span></span>|<span data-ttu-id="05cfc-142">**Função**</span><span class="sxs-lookup"><span data-stu-id="05cfc-142">**Function**</span></span>|<span data-ttu-id="05cfc-143">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="05cfc-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05cfc-144">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="05cfc-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="05cfc-145">CMyMAPIFormViewer:: GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="05cfc-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="05cfc-146">MFCMAPI usa o método **IMAPIFolder:: GetMessageStatus** para obter o status da próxima mensagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="05cfc-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="05cfc-147">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="05cfc-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="05cfc-148">OpenMessageNonModal e OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="05cfc-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="05cfc-149">MFCMAPI usa o método **IMAPIFolder:: GetMessageStatus** para obter o status da mensagem a ser exibida para passar para o Visualizador de formulários, que é CMyMAPIFormViewer ou [IMAPISession:: formulário](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="05cfc-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05cfc-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="05cfc-150">See also</span></span>



[<span data-ttu-id="05cfc-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="05cfc-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="05cfc-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="05cfc-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="05cfc-153">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="05cfc-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="05cfc-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="05cfc-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="05cfc-155">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="05cfc-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

