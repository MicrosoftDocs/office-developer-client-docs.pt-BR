---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350985"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="04600-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="04600-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="04600-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04600-105">Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais das mensagens da pasta e gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="04600-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04600-106">Parameters</span></span>

<span data-ttu-id="04600-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="04600-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="04600-108">no Um ponteiro para uma matriz de [](entrylist.md) estruturas ENTRYLIST que identificam a mensagem ou mensagens que têm sinalizadores de leitura para definir ou desmarcar.</span><span class="sxs-lookup"><span data-stu-id="04600-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="04600-109">Se _lpMsgList_ estiver definido como NULL, os sinalizadores de leitura para todas as mensagens da pasta serão definidos ou apagados.</span><span class="sxs-lookup"><span data-stu-id="04600-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="04600-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="04600-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="04600-111">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="04600-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="04600-112">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="04600-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="04600-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="04600-113">_lpProgress_</span></span>
  
> <span data-ttu-id="04600-114">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="04600-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="04600-115">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do MAPI.</span><span class="sxs-lookup"><span data-stu-id="04600-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="04600-116">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="04600-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="04600-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04600-117">_ulFlags_</span></span>
  
> <span data-ttu-id="04600-118">no Uma bitmask de sinalizadores que controla a configuração do sinalizador de leitura de uma mensagem e o processamento de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="04600-119">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="04600-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="04600-120">CLEAR_READ_FLAG: o sinalizador MSGFLAG_READ deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório de leitura não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="04600-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="04600-121">CLEAR_NRN_PENDING: o sinalizador MSGFLAG_NRN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório não lido não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="04600-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="04600-122">CLEAR_RN_PENDING: o sinalizador MSGFLAG_RN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório de leitura não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="04600-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="04600-123">GENERATE_RECEIPT_ONLY: um relatório de leitura deverá ser enviado se um estiver pendente, mas não houver nenhuma alteração no estado do sinalizador MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="04600-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="04600-124">MAPI_DEFERRED_ERRORS: permite que o **SetReadFlags** seja retornado com êxito, possivelmente antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="04600-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="04600-125">MESSAGE_DIALOG: exibe um indicador de progresso enquanto a operação prossegue.</span><span class="sxs-lookup"><span data-stu-id="04600-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="04600-126">SUPPRESS_RECEIPT: um relatório de leitura pendente deve ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada alterar o estado da mensagem de não lidos para leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="04600-127">Se essa chamada não alterar o estado da mensagem, o provedor de repositório de mensagens poderá ignorar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="04600-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="04600-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="04600-128">Return values</span></span>

<span data-ttu-id="04600-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="04600-129">S_OK</span></span> 
  
> <span data-ttu-id="04600-130">O sinalizador de leitura para a mensagem ou mensagens especificadas foi definido ou limpo com êxito.</span><span class="sxs-lookup"><span data-stu-id="04600-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="04600-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="04600-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="04600-132">O provedor de repositório de mensagens não oferece suporte à supressão de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="04600-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="04600-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="04600-134">Uma das seguintes combinações incompatíveis de sinalizadores é definida no parâmetro _parâmetroulflags_ :</span><span class="sxs-lookup"><span data-stu-id="04600-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="04600-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="04600-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="04600-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="04600-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="04600-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="04600-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="04600-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="04600-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="04600-139">A chamada teve êxito, mas nem todas as mensagens foram processadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="04600-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="04600-140">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="04600-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="04600-141">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="04600-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="04600-142">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="04600-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04600-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="04600-143">Remarks</span></span>

<span data-ttu-id="04600-144">O método **IMAPIFolder:: SetReadFlags** define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de uma ou mais das mensagens da pasta.</span><span class="sxs-lookup"><span data-stu-id="04600-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="04600-145">Definir o sinalizador MSGFLAG_READ marca uma mensagem como lida, o que não indica necessariamente que o destinatário pretendido realmente leu a mensagem.</span><span class="sxs-lookup"><span data-stu-id="04600-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="04600-146">O **SetReadFlags** também gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="04600-147">O sinalizador de leitura não pode ser alterado para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04600-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="04600-148">Mensagens que não existem.</span><span class="sxs-lookup"><span data-stu-id="04600-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="04600-149">Mensagens que foram movidas em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="04600-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="04600-150">Mensagens abertas com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="04600-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="04600-151">Mensagens que estão sendo enviadas.</span><span class="sxs-lookup"><span data-stu-id="04600-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="04600-152">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="04600-152">Notes to implementers</span></span>

<span data-ttu-id="04600-153">Você pode decidir não oferecer suporte ao envio de relatórios de leitura e à solicitação para suprimir relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="04600-154">Para evitar a supressão de um relatório de leitura, retorne MAPI_E_NO_SUPPRESS quando **SetReadFlags** for chamado com SUPPRESS_RECEIPT definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="04600-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="04600-155">Quando o parâmetro _lpMsgList_ aponta para mais de uma mensagem, execute a operação o mais completo possível para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="04600-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="04600-156">Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04600-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="04600-157">Se nenhum dos sinalizadores estiver definido no parâmetro _parâmetroulflags_ , as seguintes regras serão aplicadas:</span><span class="sxs-lookup"><span data-stu-id="04600-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="04600-158">Se MSGFLAG_READ já estiver definido, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="04600-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="04600-159">Se MSGFLAG_READ não estiver definido, defina-o imediatamente e envie quaisquer relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.</span><span class="sxs-lookup"><span data-stu-id="04600-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="04600-160">Quando o sinalizador SUPPRESS_RECEIPT é definido, as seguintes regras são aplicadas:</span><span class="sxs-lookup"><span data-stu-id="04600-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="04600-161">Se MSGFLAG_READ já estiver definido, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="04600-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="04600-162">Se MSGFLAG_READ não estiver definido, defina-o e cancele todos os relatórios de leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="04600-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="04600-163">Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de cada mensagem e não envie relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="04600-164">Quando o sinalizador GENERATE_RECEIPT_ONLY estiver definido, envie quaisquer relatórios de leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="04600-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="04600-165">Não defina ou desmarque MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="04600-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="04600-166">Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estiverem definidos, defina **PR_READ_RECEIPT_REQUESTED** como false se ele estiver definido e não enviar um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="04600-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="04600-167">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="04600-167">Notes to callers</span></span>

<span data-ttu-id="04600-168">Espere estes valores de retorno sob as condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="04600-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="04600-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="04600-169">**Condition**</span></span>|<span data-ttu-id="04600-170">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="04600-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04600-171">**SetReadFlags** processou com êxito todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="04600-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="04600-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="04600-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="04600-173">O **SetReadFlags** não pôde processar com êxito todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="04600-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="04600-174">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="04600-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="04600-175">**SetReadFlags** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="04600-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="04600-176">Qualquer valor de erro, exceto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="04600-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="04600-177">Quando o **SetReadFlags** não puder ser concluído, não presuma que nenhum trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="04600-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="04600-178">**SetReadFlags** pode ter sido capaz de definir ou desmarcar o sinalizador MSGFLAG_READ para uma ou mais das mensagens antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="04600-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="04600-179">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="04600-179">MFCMAPI reference</span></span>

<span data-ttu-id="04600-180">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="04600-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="04600-181">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="04600-181">**File**</span></span>|<span data-ttu-id="04600-182">**Função**</span><span class="sxs-lookup"><span data-stu-id="04600-182">**Function**</span></span>|<span data-ttu-id="04600-183">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="04600-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04600-184">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="04600-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="04600-185">CFolderDlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="04600-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="04600-186">MFCMAPI usa o método **IMAPIFolder:: SetReadFlags** para definir manualmente o status de leitura nas mensagens especificadas.</span><span class="sxs-lookup"><span data-stu-id="04600-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04600-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="04600-187">See also</span></span>

- [<span data-ttu-id="04600-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="04600-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="04600-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="04600-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="04600-190">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="04600-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="04600-191">Propriedade canônica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="04600-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="04600-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="04600-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="04600-193">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="04600-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="04600-194">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="04600-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

