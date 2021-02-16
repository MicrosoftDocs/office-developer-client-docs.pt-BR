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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406910"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="3b6bf-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="3b6bf-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="3b6bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b6bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b6bf-105">Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais mensagens da pasta e gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3b6bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b6bf-106">Parameters</span></span>

<span data-ttu-id="3b6bf-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="3b6bf-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="3b6bf-108">[in] Um ponteiro para uma matriz de [estruturas ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens que têm sinalizadores de leitura a definir ou limpar.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="3b6bf-109">Se  _lpMsgList_ for definido como NULL, os sinalizadores de leitura de todas as mensagens da pasta serão definidos ou limpos.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="3b6bf-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3b6bf-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="3b6bf-111">[in] Um alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="3b6bf-112">O _parâmetro ulUIParam é_ ignorado, a menos que o MESSAGE_DIALOG padrão seja definido no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="3b6bf-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="3b6bf-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="3b6bf-113">_lpProgress_</span></span>
  
> <span data-ttu-id="3b6bf-114">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="3b6bf-115">Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="3b6bf-116">O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido em  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="3b6bf-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b6bf-117">_ulFlags_</span></span>
  
> <span data-ttu-id="3b6bf-118">[in] Uma máscara de bits de sinalizadores que controla a configuração do sinalizador de leitura de uma mensagem e o processamento de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="3b6bf-119">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="3b6bf-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="3b6bf-120">CLEAR_READ_FLAG: o MSGFLAG_READ sinalizador deve ser limpo **PR_MESSAGE_FLAGS** um relatório de leitura não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="3b6bf-121">CLEAR_NRN_PENDING: o MSGFLAG_NRN_PENDING deve ser limpo **PR_MESSAGE_FLAGS** relatório não lido não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="3b6bf-122">CLEAR_RN_PENDING: o MSGFLAG_RN_PENDING sinalizador deve ser limpo **PR_MESSAGE_FLAGS** um relatório de leitura não deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="3b6bf-123">GENERATE_RECEIPT_ONLY: um relatório de leitura deve ser enviado se houver um pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="3b6bf-124">MAPI_DEFERRED_ERRORS: permite que **SetReadFlags** retorne com êxito, possivelmente antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="3b6bf-125">MESSAGE_DIALOG: exibe um indicador de progresso enquanto a operação continua.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="3b6bf-126">SUPPRESS_RECEIPT: um relatório de leitura pendente deverá ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada mudar o estado da mensagem de não lida para lida.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="3b6bf-127">Se essa chamada não alterar o estado da mensagem, o provedor do armazenamento de mensagens poderá ignorar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="3b6bf-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b6bf-128">Return values</span></span>

<span data-ttu-id="3b6bf-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b6bf-129">S_OK</span></span> 
  
> <span data-ttu-id="3b6bf-130">O sinalizador de leitura da mensagem ou mensagens especificada foi definido ou limpo com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="3b6bf-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="3b6bf-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="3b6bf-132">O provedor de armazenamento de mensagens não suporta a supressão de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="3b6bf-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3b6bf-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="3b6bf-134">Uma das seguintes combinações incompatíveis de sinalizadores é definida no _parâmetro ulFlags:_</span><span class="sxs-lookup"><span data-stu-id="3b6bf-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="3b6bf-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="3b6bf-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="3b6bf-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="3b6bf-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="3b6bf-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="3b6bf-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="3b6bf-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="3b6bf-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="3b6bf-139">A chamada foi bem-sucedida, mas nem todas as mensagens foram processadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="3b6bf-140">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="3b6bf-141">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="3b6bf-142">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="3b6bf-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b6bf-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b6bf-143">Remarks</span></span>

<span data-ttu-id="3b6bf-144">O **método IMAPIFolder::SetReadFlags** define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de uma ou mais mensagens da pasta.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="3b6bf-145">Definir o MSGFLAG_READ marca uma mensagem como lida, o que não indica necessariamente que o destinatário pretendido realmente leu a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="3b6bf-146">**SetReadFlags** também gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="3b6bf-147">O sinalizador de leitura não pode ser alterado para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3b6bf-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="3b6bf-148">Mensagens que não existem.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="3b6bf-149">Mensagens que foram movidas para outro lugar.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="3b6bf-150">Mensagens abertas com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="3b6bf-151">Mensagens enviadas no momento.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="3b6bf-152">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="3b6bf-152">Notes to implementers</span></span>

<span data-ttu-id="3b6bf-153">Você pode decidir não suportar o envio de relatórios de leitura e a solicitação para suprimir relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="3b6bf-154">Para evitar suprimir um relatório de leitura, retorne MAPI_E_NO_SUPPRESS quando **SetReadFlags** for chamado com SUPPRESS_RECEIPT definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="3b6bf-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="3b6bf-155">Quando o  _parâmetro lpMsgList_ aponta para mais de uma mensagem, execute a operação o mais completamente possível para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="3b6bf-156">Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do controle, como falta de memória, falta de espaço em disco ou corrupção no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="3b6bf-157">Se nenhum dos sinalizadores for definido no  _parâmetro ulFlags,_ as seguintes regras serão aplicadas:</span><span class="sxs-lookup"><span data-stu-id="3b6bf-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="3b6bf-158">Se MSGFLAG_READ já estiver definido, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="3b6bf-159">Se MSGFLAG_READ não estiver definida, de definida imediatamente e envie relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="3b6bf-160">Quando o SUPPRESS_RECEIPT sinalizador estiver definido, as seguintes regras serão aplicadas:</span><span class="sxs-lookup"><span data-stu-id="3b6bf-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="3b6bf-161">Se MSGFLAG_READ já estiver definido, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="3b6bf-162">Se MSGFLAG_READ não estiver definido, de definida-a e cancele quaisquer relatórios de leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="3b6bf-163">Quando o CLEAR_READ_FLAG sinalizador estiver definido, limpe o sinalizador MSGFLAG_READ na  propriedade PR_MESSAGE_FLAGS de cada mensagem e não envie nenhum relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="3b6bf-164">Quando o GENERATE_RECEIPT_ONLY sinalizador estiver definido, envie relatórios de leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="3b6bf-165">Não de definir ou limpar MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="3b6bf-166">Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estão definidos,  de definida PR_READ_RECEIPT_REQUESTED como FALSE se estiver definida e não enviar um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3b6bf-167">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3b6bf-167">Notes to callers</span></span>

<span data-ttu-id="3b6bf-168">Espere esses valores de retorno sob as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="3b6bf-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="3b6bf-169">**Condition**</span></span>|<span data-ttu-id="3b6bf-170">**Valor de retorno**</span><span class="sxs-lookup"><span data-stu-id="3b6bf-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b6bf-171">**SetReadFlags** processou todas as mensagens com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="3b6bf-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b6bf-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="3b6bf-173">**SetReadFlags** não pôde processar todas as mensagens com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="3b6bf-174">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3b6bf-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="3b6bf-175">**SetReadFlags** não pôde ser concluído.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="3b6bf-176">Qualquer valor de erro, exceto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3b6bf-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="3b6bf-177">Quando **SetReadFlags** não puder ser concluído, não suponha que nenhum trabalho foi feito.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="3b6bf-178">**SetReadFlags** pode ter sido capaz de definir ou limpar o sinalizador de MSGFLAG_READ para uma ou mais mensagens antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b6bf-179">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3b6bf-179">MFCMAPI reference</span></span>

<span data-ttu-id="3b6bf-180">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b6bf-181">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3b6bf-181">**File**</span></span>|<span data-ttu-id="3b6bf-182">**Função**</span><span class="sxs-lookup"><span data-stu-id="3b6bf-182">**Function**</span></span>|<span data-ttu-id="3b6bf-183">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="3b6bf-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b6bf-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3b6bf-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="3b6bf-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="3b6bf-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="3b6bf-186">MFCMAPI usa o **método IMAPIFolder::SetReadFlags** para definir manualmente o status de leitura nas mensagens especificadas.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b6bf-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b6bf-187">See also</span></span>

- [<span data-ttu-id="3b6bf-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="3b6bf-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="3b6bf-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="3b6bf-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="3b6bf-190">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="3b6bf-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="3b6bf-191">Propriedade canônica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3b6bf-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="3b6bf-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3b6bf-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="3b6bf-193">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="3b6bf-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="3b6bf-194">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="3b6bf-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

