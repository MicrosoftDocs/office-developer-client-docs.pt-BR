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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423318"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="3b7a5-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="3b7a5-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="3b7a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b7a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b7a5-105">Indica que o spooler MAPI tem uma mensagem para o provedor de transporte entregar.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="3b7a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b7a5-106">Parameters</span></span>

 <span data-ttu-id="3b7a5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b7a5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3b7a5-108">[in] Uma máscara de bits de sinalizadores que controla como a mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="3b7a5-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3b7a5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3b7a5-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="3b7a5-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="3b7a5-111">O spooler MAPI está chamando um provedor de transporte com uma mensagem que foi adiada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="3b7a5-112">O identificador de entrada da mensagem é o mesmo de quando ela foi adiada.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="3b7a5-113">A mensagem foi adiada passando seu identificador de entrada de volta para o spooler MAPI usando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED usuário.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="3b7a5-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3b7a5-114">_lpMessage_</span></span>
  
> <span data-ttu-id="3b7a5-115">[in] Um ponteiro para um objeto de mensagem (representando a mensagem a ser entregue) que tem permissão de leitura/gravação, que o provedor de transporte usa para acessar e manipular essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="3b7a5-116">Esse objeto permanece válido até que o provedor de transporte retorne de uma chamada subsequente para o [método IXPLogon::EndMessage.](ixplogon-endmessage.md)</span><span class="sxs-lookup"><span data-stu-id="3b7a5-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="3b7a5-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="3b7a5-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="3b7a5-118">[out] Um ponteiro para uma variável na qual o provedor de transporte retorna o valor de referência atribuído a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="3b7a5-119">O spooler MAPI passa esse valor de referência em chamadas subsequentes para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="3b7a5-120">O spooler MAPI inicializa o valor como 0 antes de retorá-lo para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="3b7a5-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="3b7a5-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="3b7a5-122">[out] Um ponteiro para uma variável que corresponde ao valor MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR de erro retornado por **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b7a5-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b7a5-123">Return value</span></span>

<span data-ttu-id="3b7a5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b7a5-124">S_OK</span></span> 
  
> <span data-ttu-id="3b7a5-125">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="3b7a5-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3b7a5-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3b7a5-127">O provedor de transporte não pode manipular a mensagem, pois está executando outra operação.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="3b7a5-128">Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o spooler MAPI não deve chamar **EndMessage**.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="3b7a5-129">O spooler MAPI tentará a **chamada SubmitMessage** novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="3b7a5-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="3b7a5-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="3b7a5-131">Embora o provedor de transporte tenha solicitado que o spooler MAPI resubmita a mensagem em uma chamada **SpoolerNotify** anterior, as condições foram alteradas desde então e a mensagem não deve ser reemitida.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="3b7a5-132">O spooler MAPI passará a tratar de outra coisa.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="3b7a5-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="3b7a5-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="3b7a5-134">Um erro de rede impede a conclusão bem-sucedida da operação.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="3b7a5-135">O  _parâmetro lpulReturnParm_ deve ser definido como o número de segundos que passará antes que o spooler MAPI resubmita a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="3b7a5-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="3b7a5-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="3b7a5-137">O provedor de transporte não pode lidar com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="3b7a5-138">O spooler MAPI deve tentar encontrar outro provedor de transporte para ele.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="3b7a5-139">Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o spooler MAPI não deve chamar **EndMessage**.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="3b7a5-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="3b7a5-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="3b7a5-141">Um problema temporário impede que o provedor de transporte manipular a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="3b7a5-142">O  _parâmetro lpulReturnParm_ deve ser definido como o número de segundos que passará antes que o spooler MAPI resubmita a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3b7a5-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b7a5-143">Remarks</span></span>

<span data-ttu-id="3b7a5-144">O spooler MAPI chama o método **IXPLogon::SubmitMessage** quando ele tem uma mensagem para o provedor de transporte entregar.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="3b7a5-145">A mensagem é passada para o provedor de transporte usando o _parâmetro lpMessage._</span><span class="sxs-lookup"><span data-stu-id="3b7a5-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="3b7a5-146">Se o provedor estiver pronto para aceitar a mensagem, ele deverá retornar um valor de referência usando o parâmetro  _lpulMsgRef,_ processar o objeto passado e retornar o valor apropriado (geralmente S_OK).</span><span class="sxs-lookup"><span data-stu-id="3b7a5-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="3b7a5-147">Se o provedor não estiver preparado para lidar com a transferência, ele deverá retornar um valor de erro e, opcionalmente, outro valor de retorno MAPI em  _lpulReturnParm_ para indicar quanto tempo o spooler MAPI deve aguardar antes de reemitir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="3b7a5-148">A implementação desse método por um provedor de transporte pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3b7a5-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="3b7a5-149">Coloque a mensagem em uma fila interna para aguardar a transmissão, possivelmente copiando a mensagem para o armazenamento local e retorne.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="3b7a5-150">Tente executar a transmissão real e retornar quando a transmissão for concluída, com êxito ou sem êxito.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="3b7a5-151">Determine se a mensagem será enviada após a verificação do recurso envolvido.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="3b7a5-152">Nesse caso, se o recurso estiver livre, o provedor poderá bloquear o recurso, preparar a mensagem e encaminhá-la.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="3b7a5-153">Se o recurso estiver ocupado, o provedor poderá preparar a mensagem e adiar o envio para uma hora posterior.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="3b7a5-154">A técnica preferida para transmissão de mensagens depende do provedor de transporte e do número esperado de processos que competem por recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="3b7a5-155">Durante uma **chamada SubmitMessage,** o provedor de transporte controla a transferência de dados de mensagem do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="3b7a5-156">No entanto, o provedor de transporte deve atribuir um valor de referência à mensagem, ao qual retorna um ponteiro em  _lpulMsgRef_, antes de transferir dados.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="3b7a5-157">Isso acontece porque, a qualquer momento durante o processo, o spooler MAPI pode chamar o método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) com o sinalizador NOTIFY_CANCEL_MESSAGE definido para sinalizar ao provedor que ele deve liberar todos os objetos abertos e interromper a transferência de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="3b7a5-158">O provedor de transporte não deve enviar nenhuma propriedade nãotransmitível da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="3b7a5-159">Quando encontrar essa propriedade, ela deverá processar a próxima propriedade.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="3b7a5-160">O provedor deve se esforçar para não exibir MAPI_P1 de destinatário como parte do conteúdo da mensagem transmitida; o provedor deve usar essas informações de destinatário somente para fins de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="3b7a5-161">MAPI_P1 destinatários são destinatários gerados internamente que são usados para reending messages; eles não devem ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="3b7a5-162">Em vez disso, use os outros destinatários para transmitir informações do destinatário.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="3b7a5-163">O objetivo dessa disposição é permitir que destinatários reend vejam exatamente a mesma tabela de destinatários que os destinatários originais.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="3b7a5-164">Durante uma **chamada SubmitMessage,** o spooler MAPI processa métodos para objetos que são abertos durante a transferência da mensagem e processa todos os anexos.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="3b7a5-165">Esse processamento pode levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-165">This processing can take a long time.</span></span> <span data-ttu-id="3b7a5-166">Os provedores de transporte podem chamar o método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o spooler MAPI frequentemente durante esse processamento para liberar tempo de CPU para outras tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="3b7a5-167">Todos os destinatários da mensagem ficam visíveis na tabela de destinatários da mensagem que o spooler MAPI originalmente passou.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="3b7a5-168">O provedor de transporte deve processar apenas os destinatários que ele pode manipular — com base no identificador de entrada, tipo de endereço ou ambos — e que ainda não têm sua propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="3b7a5-169">Se **PR_RESPONSIBILITY** já estiver definido como TRUE, outro provedor de transporte terá tratado esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="3b7a5-170">Quando o provedor concluir o processamento suficiente de um destinatário para determinar se ele pode manipular mensagens para esse destinatário, ele deve definir a propriedade **PR_RESPONSIBILITY** desse destinatário como TRUE na mensagem passada.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="3b7a5-171">Normalmente, o provedor faz essa determinação após a conclusão da entrega da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="3b7a5-172">Normalmente, o provedor de transporte não retorna de uma **chamada SubmitMessage** até concluir a transferência de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="3b7a5-173">Se nenhum erro for retornado, a próxima chamada do spooler MAPI para o provedor será uma chamada para o método [IXPLogon::EndMessage.](ixplogon-endmessage.md)</span><span class="sxs-lookup"><span data-stu-id="3b7a5-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="3b7a5-174">Se **SubmitMessage retornar** um erro, o spooler MAPI liberará a mensagem em processo sem salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="3b7a5-175">Se o provedor de transporte exigir que as alterações de mensagem sejam salvas, ele deverá chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="3b7a5-176">Em caso de erros que ocorrem devido a problemas de transporte, o spooler MAPI retém a mensagem, mas atrasa a resubmissão da mensagem para o provedor de transporte com base no valor retornado em  _lpulReturnParm_.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="3b7a5-177">O provedor de transporte deverá preencher esse valor se o valor de retorno de **SubmitMessage** for MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="3b7a5-178">Se ocorrer uma condição de erro grave, o provedor de transporte deverá chamar o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_CRITICAL_ERROR usuário.</span><span class="sxs-lookup"><span data-stu-id="3b7a5-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b7a5-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b7a5-179">See also</span></span>



[<span data-ttu-id="3b7a5-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="3b7a5-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="3b7a5-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="3b7a5-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="3b7a5-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="3b7a5-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="3b7a5-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="3b7a5-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="3b7a5-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="3b7a5-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="3b7a5-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b7a5-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

