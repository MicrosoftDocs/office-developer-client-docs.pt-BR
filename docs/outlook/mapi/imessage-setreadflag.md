---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439867"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="e4067-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="e4067-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="e4067-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4067-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4067-105">Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem e gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e4067-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4067-106">Parameters</span></span>

<span data-ttu-id="e4067-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4067-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e4067-108">no Bitmask de sinalizadores que controlam a configuração do sinalizador de leitura de uma mensagem ou seja, o sinalizador MSGFLAG_READ da mensagem em sua propriedade **PR_MESSAGE_FLAGS** e o processamento de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="e4067-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e4067-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="e4067-110">CLEAR_READ_FLAG: o sinalizador MSGFLAG_READ deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório de leitura deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="e4067-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="e4067-111">CLEAR_NRN_PENDING: o sinalizador MSGFLAG_NRN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório de não leitura não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="e4067-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="e4067-112">CLEAR_RN_PENDING: o sinalizador MSGFLAG_RN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório de leitura deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="e4067-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="e4067-113">GENERATE_RECEIPT_ONLY: um relatório de leitura deverá ser enviado se um estiver pendente, mas não houver nenhuma alteração no estado do sinalizador MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="e4067-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="e4067-114">MAPI_DEFERRED_ERRORS: permite que o **SetReadFlag** seja retornado com êxito, possivelmente antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="e4067-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="e4067-115">SUPPRESS_RECEIPT: um relatório de leitura pendente deve ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada alterar o estado da mensagem de não lidos para leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="e4067-116">Se essa chamada não alterar o estado da mensagem, o provedor de repositório de mensagens poderá ignorar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e4067-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4067-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e4067-117">Return value</span></span>

<span data-ttu-id="e4067-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4067-118">S_OK</span></span> 
  
> <span data-ttu-id="e4067-119">O sinalizador de leitura da mensagem foi definido ou limpo com êxito.</span><span class="sxs-lookup"><span data-stu-id="e4067-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="e4067-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="e4067-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="e4067-121">O provedor de repositório de mensagens não oferece suporte à supressão de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="e4067-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4067-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e4067-123">Uma das seguintes combinações de sinalizadores é definida no parâmetro _parâmetroulflags_ :</span><span class="sxs-lookup"><span data-stu-id="e4067-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="e4067-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="e4067-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="e4067-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="e4067-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="e4067-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="e4067-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4067-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4067-127">Remarks</span></span>

<span data-ttu-id="e4067-128">O método **IMessage:: SetReadFlag** define ou limpa o sinalizador MSGFLAG_READ da mensagem na propriedade **PR_MESSAGE_FLAGS** e chama [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4067-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="e4067-129">Definir o sinalizador MSGFLAG_READ marca uma mensagem como tendo sido lida, o que não necessariamente indica que o destinatário pretendido realmente leu a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4067-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="e4067-130">O **SetReadFlags** também gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="e4067-131">Um relatório de leitura é enviado somente se o remetente solicitou um.</span><span class="sxs-lookup"><span data-stu-id="e4067-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="e4067-132">O sinalizador de leitura não pode ser alterado para:</span><span class="sxs-lookup"><span data-stu-id="e4067-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="e4067-133">Mensagens que não existem.</span><span class="sxs-lookup"><span data-stu-id="e4067-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="e4067-134">Mensagens que foram movidas em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="e4067-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="e4067-135">Mensagens abertas com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e4067-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="e4067-136">Mensagens que estão sendo enviadas.</span><span class="sxs-lookup"><span data-stu-id="e4067-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="e4067-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e4067-137">Notes to callers</span></span>

<span data-ttu-id="e4067-138">Se nenhum dos sinalizadores estiver definido no parâmetro _parâmetroulflags_ , as seguintes regras serão aplicadas:</span><span class="sxs-lookup"><span data-stu-id="e4067-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="e4067-139">Se MSGFLAG_READ já estiver definido, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="e4067-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="e4067-140">Se MSGFLAG_READ não estiver definido, defina-o e envie quaisquer relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.</span><span class="sxs-lookup"><span data-stu-id="e4067-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="e4067-141">Se os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estiverem definidos, o bit PR_READ_RECEIPT_REQUESTED, se definido, deverá ser limpo e um relatório de leitura não deverá ser enviado.</span><span class="sxs-lookup"><span data-stu-id="e4067-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="e4067-142">Quando o sinalizador SUPPRESS_RECEIPT estiver definido:</span><span class="sxs-lookup"><span data-stu-id="e4067-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="e4067-143">Se MSGFLAG_READ já estiver definido, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="e4067-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="e4067-144">Se MSGFLAG_READ não estiver definido, defina-o e cancele todos os relatórios de leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="e4067-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="e4067-145">Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de cada mensagem e não envie relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="e4067-146">Quando o sinalizador GENERATE_RECEIPT_ONLY estiver definido, envie quaisquer relatórios de leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="e4067-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="e4067-147">Não defina ou desmarque MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="e4067-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="e4067-148">Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estiverem definidos, defina a propriedade PR_READ_RECEIPT_REQUESTED como FALSE se ela estiver definida e não enviar um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="e4067-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="e4067-149">Você pode otimizar o comportamento do relatório eliminando a geração de relatórios de leitura sob determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="e4067-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="e4067-150">No enTanto, se você não oferecer suporte à supressão de relatórios e um cliente chama **SetReadFlag** com o sinalizador SUPPRESS_RECEIPT definido, retorne MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="e4067-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e4067-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e4067-151">MFCMAPI reference</span></span>

<span data-ttu-id="e4067-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4067-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e4067-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e4067-153">**File**</span></span>|<span data-ttu-id="e4067-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="e4067-154">**Function**</span></span>|<span data-ttu-id="e4067-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e4067-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4067-156">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="e4067-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="e4067-157">CFolderDlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="e4067-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="e4067-158">MFCMAPI usa o método **IMessage:: SetReadFlag** para definir sinalizadores de leitura em mensagens selecionadas.</span><span class="sxs-lookup"><span data-stu-id="e4067-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4067-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4067-159">See also</span></span>

- [<span data-ttu-id="e4067-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e4067-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="e4067-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="e4067-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="e4067-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e4067-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="e4067-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e4067-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="e4067-164">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="e4067-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="e4067-165">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e4067-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="e4067-166">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e4067-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

