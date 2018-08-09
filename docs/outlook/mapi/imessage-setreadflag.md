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
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767388"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="394bf-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="394bf-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="394bf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="394bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="394bf-105">Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem e gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="394bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="394bf-106">Parameters</span></span>

<span data-ttu-id="394bf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="394bf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="394bf-108">[in] Bitmask dos sinalizadores que controla a definição da leitura da mensagem ou seja, sinalizador sinalizador MSGFLAG_READ da mensagem em sua propriedade **PR_MESSAGE_FLAGS** e o processamento de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="394bf-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="394bf-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="394bf-110">CLEAR_READ_FLAG: O sinalizador MSGFLAG_READ deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório leitura deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="394bf-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="394bf-111">CLEAR_NRN_PENDING: O sinalizador MSGFLAG_NRN_PENDING deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório de não-leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="394bf-112">CLEAR_RN_PENDING: O sinalizador MSGFLAG_RN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório leitura deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="394bf-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="394bf-113">GENERATE_RECEIPT_ONLY: Um relatório de leitura deverão ser enviado se um está pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="394bf-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="394bf-114">MAPI_DEFERRED_ERRORS: Permite **SetReadFlag** retornar com êxito, possivelmente antes que a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="394bf-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="394bf-115">SUPPRESS_RECEIPT: Um relatório de leitura pendente deve ser cancelado se um relatório de leitura tivesse sido solicitado e essa chamada altera o estado da mensagem de não lido para ler.</span><span class="sxs-lookup"><span data-stu-id="394bf-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="394bf-116">Se essa chamada não alterar o estado da mensagem, o provedor de armazenamento de mensagem pode ignorar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="394bf-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="394bf-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="394bf-117">Return value</span></span>

<span data-ttu-id="394bf-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="394bf-118">S_OK</span></span> 
  
> <span data-ttu-id="394bf-119">Sinalizador de leitura da mensagem foi definida com êxito ou desmarcada.</span><span class="sxs-lookup"><span data-stu-id="394bf-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="394bf-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="394bf-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="394bf-121">O provedor de armazenamento de mensagem não suporta a supressão de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="394bf-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="394bf-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="394bf-123">Uma das seguintes combinações de sinalizadores está definida no parâmetro _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="394bf-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="394bf-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="394bf-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="394bf-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="394bf-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="394bf-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="394bf-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="394bf-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="394bf-127">Remarks</span></span>

<span data-ttu-id="394bf-128">O método **IMessage::SetReadFlag** define ou limpa o sinalizador MSGFLAG_READ da mensagem na propriedade **PR_MESSAGE_FLAGS** e chamadas [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="394bf-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="394bf-129">Definindo o sinalizador MSGFLAG_READ marca uma mensagem como tendo sido lida, que não necessariamente indica que o destinatário pretendido realmente leu a mensagem.</span><span class="sxs-lookup"><span data-stu-id="394bf-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="394bf-130">**SetReadFlags** também gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="394bf-131">Um relatório de leitura é enviado somente se o remetente solicitou uma.</span><span class="sxs-lookup"><span data-stu-id="394bf-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="394bf-132">O sinalizador de leitura não pode ser alterado para:</span><span class="sxs-lookup"><span data-stu-id="394bf-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="394bf-133">Mensagens que não existem.</span><span class="sxs-lookup"><span data-stu-id="394bf-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="394bf-134">Mensagens que foram movidas para outro lugar.</span><span class="sxs-lookup"><span data-stu-id="394bf-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="394bf-135">Mensagens que estão abertas com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="394bf-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="394bf-136">Mensagens que atualmente são enviadas.</span><span class="sxs-lookup"><span data-stu-id="394bf-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="394bf-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="394bf-137">Notes to callers</span></span>

<span data-ttu-id="394bf-138">Se nenhum dos sinalizadores estão definidos no parâmetro _ulFlags_ , as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="394bf-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="394bf-139">Se MSGFLAG_READ já estiver definida, nada a fazer.</span><span class="sxs-lookup"><span data-stu-id="394bf-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="394bf-140">Se MSGFLAG_READ não estiver definida, defini-la e enviar pendentes de relatórios de leitura, se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) é definida.</span><span class="sxs-lookup"><span data-stu-id="394bf-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="394bf-141">Se os SUPPRESS_RECEIPT GENERATE_RECEIPT_ONLY sinalizadores e estiverem definidos, o PR_READ_RECEIPT_REQUESTED bit, se definido, deve ser limpo e não deve ser enviado a um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="394bf-142">Quando o sinalizador SUPPRESS_RECEIPT é definido:</span><span class="sxs-lookup"><span data-stu-id="394bf-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="394bf-143">Se MSGFLAG_READ já estiver definida, nada a fazer.</span><span class="sxs-lookup"><span data-stu-id="394bf-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="394bf-144">Se MSGFLAG_READ não estiver definida, defini-la e Cancelar pendentes de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="394bf-145">Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** do cada mensagem e não enviar todos os relatórios leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="394bf-146">Quando o sinalizador GENERATE_RECEIPT_ONLY é definido, envie todos os relatórios leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="394bf-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="394bf-147">Faça MSGFLAG_READ não definir ou limpar.</span><span class="sxs-lookup"><span data-stu-id="394bf-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="394bf-148">Quando os SUPPRESS_RECEIPT GENERATE_RECEIPT_ONLY sinalizadores e estiverem definidos, defina a propriedade PR_READ_RECEIPT_REQUESTED como FALSE se estiver definida e não enviar um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="394bf-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="394bf-149">Você pode otimizar o comportamento de relatório por suprimindo a geração de relatórios de leitura sob certas condições.</span><span class="sxs-lookup"><span data-stu-id="394bf-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="394bf-150">No entanto, se você não oferecem suporte a supressão de relatórios e um cliente chama **SetReadFlag** com o sinalizador SUPPRESS_RECEIPT definido, retorne MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="394bf-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="394bf-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="394bf-151">MFCMAPI reference</span></span>

<span data-ttu-id="394bf-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="394bf-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="394bf-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="394bf-153">**File**</span></span>|<span data-ttu-id="394bf-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="394bf-154">**Function**</span></span>|<span data-ttu-id="394bf-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="394bf-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="394bf-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="394bf-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="394bf-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="394bf-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="394bf-158">MFCMAPI usa o método **IMessage::SetReadFlag** para definir sinalizadores de leitura em mensagens selecionadas.</span><span class="sxs-lookup"><span data-stu-id="394bf-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="394bf-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="394bf-159">See also</span></span>

- [<span data-ttu-id="394bf-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="394bf-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="394bf-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="394bf-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="394bf-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="394bf-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="394bf-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="394bf-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="394bf-164">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="394bf-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="394bf-165">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="394bf-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="394bf-166">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="394bf-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

