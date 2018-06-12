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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766987"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="511be-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="511be-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="511be-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="511be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="511be-105">Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais das mensagens da pasta e gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="511be-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="511be-106">Parameters</span></span>

<span data-ttu-id="511be-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="511be-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="511be-108">[in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens que leu sinalizadores para definir ou limpar.</span><span class="sxs-lookup"><span data-stu-id="511be-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="511be-109">Se _lpMsgList_ for definido como NULL, leia sinalizadores para todas as mensagens da pasta são definidas ou desmarcadas.</span><span class="sxs-lookup"><span data-stu-id="511be-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="511be-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="511be-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="511be-111">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="511be-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="511be-112">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="511be-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="511be-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="511be-113">_lpProgress_</span></span>
  
> <span data-ttu-id="511be-114">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="511be-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="511be-115">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação do MAPI.</span><span class="sxs-lookup"><span data-stu-id="511be-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="511be-116">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="511be-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="511be-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="511be-117">_ulFlags_</span></span>
  
> <span data-ttu-id="511be-118">[in] Uma bitmask dos sinalizadores que controla a configuração de sinalizador de leitura da mensagem e o processamento de ler relatórios.</span><span class="sxs-lookup"><span data-stu-id="511be-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="511be-119">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="511be-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="511be-120">CLEAR_READ_FLAG: O sinalizador MSGFLAG_READ deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="511be-121">CLEAR_NRN_PENDING: O sinalizador MSGFLAG_NRN_PENDING deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório não lido.</span><span class="sxs-lookup"><span data-stu-id="511be-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="511be-122">CLEAR_RN_PENDING: O sinalizador MSGFLAG_RN_PENDING deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="511be-123">GENERATE_RECEIPT_ONLY: Um relatório de leitura deverão ser enviado se um está pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="511be-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="511be-124">MAPI_DEFERRED_ERRORS: Permite **SetReadFlags** retornar com êxito, possivelmente antes que a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="511be-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="511be-125">MESSAGE_DIALOG: Exibe um indicador de progresso enquanto continua a operação.</span><span class="sxs-lookup"><span data-stu-id="511be-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="511be-126">SUPPRESS_RECEIPT: Um relatório de leitura pendente deve ser cancelado se um relatório de leitura tivesse sido solicitado e essa chamada altera o estado da mensagem de não lido para ler.</span><span class="sxs-lookup"><span data-stu-id="511be-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="511be-127">Se essa chamada não alterar o estado da mensagem, o provedor de armazenamento de mensagem pode ignorar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="511be-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="511be-128">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="511be-128">Return values</span></span>

<span data-ttu-id="511be-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="511be-129">S_OK</span></span> 
  
> <span data-ttu-id="511be-130">O sinalizador de leitura para a mensagem especificada ou mensagens com êxito foi definido ou estiver desmarcado.</span><span class="sxs-lookup"><span data-stu-id="511be-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="511be-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="511be-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="511be-132">O provedor de armazenamento de mensagem não suporta a supressão de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="511be-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="511be-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="511be-134">Uma das seguintes combinações incompatíveis dos sinalizadores está definida no parâmetro _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="511be-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="511be-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="511be-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="511be-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="511be-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="511be-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="511be-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="511be-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="511be-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="511be-139">A chamada foi bem-sucedida, mas nem todas as mensagens foram processadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="511be-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="511be-140">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="511be-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="511be-141">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="511be-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="511be-142">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="511be-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="511be-143">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="511be-143">Remarks</span></span>

<span data-ttu-id="511be-144">O método **IMAPIFolder::SetReadFlags** define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de uma ou mais das mensagens da pasta.</span><span class="sxs-lookup"><span data-stu-id="511be-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="511be-145">Definindo o sinalizador MSGFLAG_READ marca uma mensagem como lida, que não necessariamente indica que o destinatário pretendido realmente leu a mensagem.</span><span class="sxs-lookup"><span data-stu-id="511be-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="511be-146">**SetReadFlags** também gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="511be-147">O sinalizador de leitura não pode ser alterado para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="511be-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="511be-148">Mensagens que não existem.</span><span class="sxs-lookup"><span data-stu-id="511be-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="511be-149">Mensagens que foram movidas para outro lugar.</span><span class="sxs-lookup"><span data-stu-id="511be-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="511be-150">Mensagens que estão abertas com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="511be-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="511be-151">Mensagens que atualmente são enviadas.</span><span class="sxs-lookup"><span data-stu-id="511be-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="511be-152">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="511be-152">Notes to implementers</span></span>

<span data-ttu-id="511be-153">Você pode decidir não suportam o envio de relatórios de leitura e a solicitação para suprimir a leitura de relatórios.</span><span class="sxs-lookup"><span data-stu-id="511be-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="511be-154">Para evitar suprimindo a um relatório de leitura, retorne MAPI_E_NO_SUPPRESS quando **SetReadFlags** é chamado com SUPPRESS_RECEIPT definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="511be-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="511be-155">Quando o parâmetro _lpMsgList_ aponta para mais de uma mensagem, execute a operação como completamente para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="511be-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="511be-156">Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="511be-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="511be-157">Se nenhum dos sinalizadores estão definidos no parâmetro _ulFlags_ , as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="511be-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="511be-158">Se MSGFLAG_READ já estiver definida, nada a fazer.</span><span class="sxs-lookup"><span data-stu-id="511be-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="511be-159">Se MSGFLAG_READ não estiver definida, defini-lo imediatamente e enviar pendentes de relatórios de leitura, se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) é definida.</span><span class="sxs-lookup"><span data-stu-id="511be-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="511be-160">Quando o sinalizador SUPPRESS_RECEIPT é definido, as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="511be-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="511be-161">Se MSGFLAG_READ já estiver definida, nada a fazer.</span><span class="sxs-lookup"><span data-stu-id="511be-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="511be-162">Se MSGFLAG_READ não estiver definida, defini-la e Cancelar pendentes de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="511be-163">Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** do cada mensagem e não enviar todos os relatórios leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="511be-164">Quando o sinalizador GENERATE_RECEIPT_ONLY é definido, envie todos os relatórios leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="511be-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="511be-165">Faça MSGFLAG_READ não definir ou limpar.</span><span class="sxs-lookup"><span data-stu-id="511be-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="511be-166">Quando os SUPPRESS_RECEIPT GENERATE_RECEIPT_ONLY sinalizadores e estiverem definidos, defina **PR_READ_RECEIPT_REQUESTED** como FALSE se ele estiver definido e não enviar um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="511be-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="511be-167">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="511be-167">Notes to callers</span></span>

<span data-ttu-id="511be-168">Espera esses valores de retorno sob as condições a seguintes.</span><span class="sxs-lookup"><span data-stu-id="511be-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="511be-169">**Condição**</span><span class="sxs-lookup"><span data-stu-id="511be-169">**Condition**</span></span>|<span data-ttu-id="511be-170">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="511be-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="511be-171">**SetReadFlags** tem processadas com êxito a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="511be-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="511be-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="511be-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="511be-173">**SetReadFlags** não pôde processar com êxito a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="511be-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="511be-174">MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="511be-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="511be-175">**SetReadFlags** não pôde concluir.</span><span class="sxs-lookup"><span data-stu-id="511be-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="511be-176">Qualquer valor de erro, exceto E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="511be-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="511be-177">Quando **SetReadFlags** é impossível concluir, não presuma que foi feito nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="511be-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="511be-178">**SetReadFlags** podem ter sido capaz de definir ou limpar o sinalizador MSGFLAG_READ para uma ou mais das mensagens antes da ocorrência de erro.</span><span class="sxs-lookup"><span data-stu-id="511be-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="511be-179">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="511be-179">MFCMAPI reference</span></span>

<span data-ttu-id="511be-180">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="511be-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="511be-181">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="511be-181">**File**</span></span>|<span data-ttu-id="511be-182">**Function**</span><span class="sxs-lookup"><span data-stu-id="511be-182">**Function**</span></span>|<span data-ttu-id="511be-183">**Comment**</span><span class="sxs-lookup"><span data-stu-id="511be-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="511be-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="511be-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="511be-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="511be-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="511be-186">MFCMAPI usa o método **IMAPIFolder::SetReadFlags** para definir manualmente o status de leitura em todas as mensagens especificadas.</span><span class="sxs-lookup"><span data-stu-id="511be-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="511be-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="511be-187">See also</span></span>

- [<span data-ttu-id="511be-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="511be-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="511be-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="511be-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="511be-190">Propriedade canônico de PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="511be-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="511be-191">Propriedade canônico de PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="511be-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="511be-192">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="511be-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="511be-193">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="511be-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="511be-194">Usando Macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="511be-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

