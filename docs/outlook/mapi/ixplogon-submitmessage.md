---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575872"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="47c80-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="47c80-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="47c80-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47c80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47c80-105">Indica que o MAPI spooler tem uma mensagem para o provedor de transporte fornecer.</span><span class="sxs-lookup"><span data-stu-id="47c80-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="47c80-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47c80-106">Parameters</span></span>

 <span data-ttu-id="47c80-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47c80-107">_ulFlags_</span></span>
  
> <span data-ttu-id="47c80-108">[in] Uma bitmask dos sinalizadores que controla como a mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="47c80-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="47c80-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="47c80-109">The following flag can be set:</span></span>
    
<span data-ttu-id="47c80-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="47c80-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="47c80-111">O MAPI spooler está chamando um provedor de transporte com uma mensagem que foi adiada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="47c80-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="47c80-112">O identificador de entrada da mensagem é o mesmo quando ele foi adiado.</span><span class="sxs-lookup"><span data-stu-id="47c80-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="47c80-113">A mensagem foi adiada passando seu identificador de entrada volta para o MAPI spooler usando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED.</span><span class="sxs-lookup"><span data-stu-id="47c80-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="47c80-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="47c80-114">_lpMessage_</span></span>
  
> <span data-ttu-id="47c80-115">[in] Um ponteiro para um objeto de mensagem (representando a entrega da mensagem) que tem a permissão de leitura/gravação, que o provedor de transporte usa para acessar e manipular a mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="47c80-116">Este objeto permanecerá válido até depois que o provedor de transporte retorna de uma chamada subsequente ao método [IXPLogon::EndMessage](ixplogon-endmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="47c80-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="47c80-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="47c80-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="47c80-118">[out] Um ponteiro para uma variável em que o provedor de transporte retornará o valor de referência atribuído a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="47c80-119">O MAPI spooler passa esse valor de referência em chamadas subsequentes para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="47c80-120">O MAPI spooler inicializa o valor como 0 antes de retorná-lo para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="47c80-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="47c80-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="47c80-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="47c80-122">[out] Um ponteiro para uma variável que corresponde ao valor de erro MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR retornado por **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="47c80-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47c80-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="47c80-123">Return value</span></span>

<span data-ttu-id="47c80-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="47c80-124">S_OK</span></span> 
  
> <span data-ttu-id="47c80-125">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="47c80-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="47c80-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="47c80-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="47c80-127">O provedor de transporte não pode manipular a mensagem, porque ele está executando outra operação.</span><span class="sxs-lookup"><span data-stu-id="47c80-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="47c80-128">Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o MAPI spooler não deve chamar **EndMessage**.</span><span class="sxs-lookup"><span data-stu-id="47c80-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="47c80-129">O MAPI spooler tentará a chamada **SubmitMessage** novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="47c80-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="47c80-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="47c80-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="47c80-131">Embora o provedor de transporte solicitado que o MAPI spooler reenviar a mensagem em uma chamada anterior de **SpoolerNotify** , condições alterou e não deve ser reenviada a mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="47c80-132">O MAPI spooler irão lidar com algo diferente.</span><span class="sxs-lookup"><span data-stu-id="47c80-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="47c80-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="47c80-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="47c80-134">Um erro de rede impediu a conclusão bem-sucedida da operação.</span><span class="sxs-lookup"><span data-stu-id="47c80-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="47c80-135">O parâmetro _lpulReturnParm_ deve ser definido como o número de segundos que decorrerá antes que o MAPI spooler reenvia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="47c80-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="47c80-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="47c80-137">O provedor de transporte não pode manipular esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="47c80-138">O MAPI spooler deve tentar localizar o outro provedor de transporte para ele.</span><span class="sxs-lookup"><span data-stu-id="47c80-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="47c80-139">Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o MAPI spooler não deve chamar **EndMessage**.</span><span class="sxs-lookup"><span data-stu-id="47c80-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="47c80-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="47c80-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="47c80-141">Um problema temporário impede que o provedor de transporte tratamento da mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="47c80-142">O parâmetro _lpulReturnParm_ deve ser definido como o número de segundos que decorrerá antes que o MAPI spooler reenvia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47c80-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="47c80-143">Remarks</span></span>

<span data-ttu-id="47c80-144">O MAPI spooler chama o método de **IXPLogon::SubmitMessage** quando ele tem uma mensagem para o provedor de transporte fornecer.</span><span class="sxs-lookup"><span data-stu-id="47c80-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="47c80-145">A mensagem será passada para o provedor de transporte usando o parâmetro _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="47c80-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="47c80-146">Se o provedor está pronto para aceitar a mensagem, ela deve retornar um valor de referência usando o parâmetro _lpulMsgRef_ , o objeto passado, de processo e retornar o valor apropriado (geralmente S_OK).</span><span class="sxs-lookup"><span data-stu-id="47c80-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="47c80-147">Se o provedor não está preparado para lidar com a transferência, ele deverá retornar um valor de erro e, opcionalmente, MAPI outro valor de retorno no _lpulReturnParm_ para indicar quanto tempo o MAPI spooler deve aguardar antes de reenviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="47c80-148">Implementação de um provedor de transporte deste método pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="47c80-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="47c80-149">Colocar a mensagem em uma fila interna para aguardar a transmissão, possivelmente copiar a mensagem para o armazenamento local e retornar.</span><span class="sxs-lookup"><span data-stu-id="47c80-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="47c80-150">Tente executar a transmissão real e retornar quando a transmissão for concluído com sucesso ou não.</span><span class="sxs-lookup"><span data-stu-id="47c80-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="47c80-151">Determine se deseja enviar a mensagem após a verificação do recurso envolvidos.</span><span class="sxs-lookup"><span data-stu-id="47c80-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="47c80-152">Nesse caso, se o recurso estiver disponível, o provedor pode bloquear o recurso, preparar a mensagem e enviá-la.</span><span class="sxs-lookup"><span data-stu-id="47c80-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="47c80-153">Se o recurso estiver ocupado, o provedor pode preparar a mensagem e adiar enviando para um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="47c80-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="47c80-154">A técnica preferida para transmissão de mensagens depende do provedor de transporte e o número esperado de processos competindo por recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="47c80-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="47c80-155">Durante uma chamada de **SubmitMessage** , o provedor de transporte controla a transferência de dados de mensagem do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="47c80-156">No entanto, o provedor de transporte deve atribuir um valor de referência para a mensagem, ao qual ele retorna um ponteiro em _lpulMsgRef_, antes de transferir os dados.</span><span class="sxs-lookup"><span data-stu-id="47c80-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="47c80-157">Ele então porque a qualquer momento durante o processo, o MAPI spooler pode chamar o método de [IXPLogon::TransportNotify](ixplogon-transportnotify.md) com o sinalizador NOTIFY_CANCEL_MESSAGE definido para sinalizar o provedor que deve liberar todos os objetos e interromper a transferência de mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="47c80-158">O provedor de transporte não deve enviar todas as propriedades nontransmittable da mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="47c80-159">Quando encontrar uma propriedade inexistente, ele deverá ir para processar a propriedade next.</span><span class="sxs-lookup"><span data-stu-id="47c80-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="47c80-160">O provedor deve fazer todos os esforços para não exibir informações do destinatário MAPI_P1 como parte do conteúdo da mensagem transmitida; o provedor deve usar essas informações de destinatário apenas para fins de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="47c80-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="47c80-161">Destinatários de MAPI_P1 são gerados internamente destinatários que são usados para reenviar mensagens; eles não devem ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="47c80-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="47c80-162">Em vez disso, use os outros destinatários para transmitir informações do destinatário.</span><span class="sxs-lookup"><span data-stu-id="47c80-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="47c80-163">A finalidade dessa organização é permitir que os destinatários de reenvio para ver a tabela de destinatários mesma exata como os destinatários originais.</span><span class="sxs-lookup"><span data-stu-id="47c80-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="47c80-164">Durante uma chamada de **SubmitMessage** , o MAPI spooler processa os métodos de objetos que estão abertos durante a transferência da mensagem e processa todos os anexos.</span><span class="sxs-lookup"><span data-stu-id="47c80-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="47c80-165">Esse processamento pode levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="47c80-165">This processing can take a long time.</span></span> <span data-ttu-id="47c80-166">Provedores de transporte podem chamar o método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o MAPI spooler frequentemente durante o processamento para liberar o tempo da CPU para outras tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="47c80-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="47c80-167">Todos os destinatários da mensagem são visíveis na tabela de destinatário da mensagem que o MAPI spooler originalmente passado.</span><span class="sxs-lookup"><span data-stu-id="47c80-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="47c80-168">O provedor de transporte deve processar somente os destinatários que pode manipular — com base no tipo de endereço, o identificador de entrada ou ambos — e que ainda não tem sua propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="47c80-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="47c80-169">Se **PR_RESPONSIBILITY** já estiver definida como TRUE, a outro provedor de transporte manipulou que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="47c80-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="47c80-170">Quando o provedor conclui o processamento suficiente de um destinatário para determinar se ele pode lidar com as mensagens para que o destinatário, ele deve definir a propriedade **PR_RESPONSIBILITY** de que o do destinatário como TRUE na mensagem passada.</span><span class="sxs-lookup"><span data-stu-id="47c80-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="47c80-171">Geralmente, o provedor torna essa determinação após a conclusão da entrega da mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="47c80-172">Normalmente, o provedor de transporte não retorna de uma chamada de **SubmitMessage** até que ele seja concluída a transferência de dados de mensagem.</span><span class="sxs-lookup"><span data-stu-id="47c80-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="47c80-173">Se nenhum erro será retornado, a próxima chamada do spooler MAPI para o provedor é uma chamada ao método [IXPLogon::EndMessage](ixplogon-endmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="47c80-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="47c80-174">Se **SubmitMessage** retornará um erro, o MAPI spooler libera a mensagem no processo sem salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="47c80-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="47c80-175">Se o provedor de transporte requer alterações de mensagem a ser salvo, ele deve chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem de antes retornando.</span><span class="sxs-lookup"><span data-stu-id="47c80-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="47c80-176">Em caso de erros que ocorrem devido a problemas de transporte, o MAPI spooler mantém a mensagem, mas ele atrasa reenviar a mensagem para o provedor de transporte com base no valor retornado no _lpulReturnParm_.</span><span class="sxs-lookup"><span data-stu-id="47c80-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="47c80-177">O provedor de transporte deve preencher esse valor se o seu valor de retorno de **SubmitMessage** é MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR.</span><span class="sxs-lookup"><span data-stu-id="47c80-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="47c80-178">Se ocorrer uma condição de erro grave, o provedor de transporte deve chamar o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_CRITICAL_ERROR.</span><span class="sxs-lookup"><span data-stu-id="47c80-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47c80-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="47c80-179">See also</span></span>



[<span data-ttu-id="47c80-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="47c80-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="47c80-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="47c80-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="47c80-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="47c80-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="47c80-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="47c80-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="47c80-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="47c80-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="47c80-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47c80-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

