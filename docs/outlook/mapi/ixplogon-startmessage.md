---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427602"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="6e01e-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="6e01e-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="6e01e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e01e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e01e-105">Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e01e-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="6e01e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e01e-106">Parameters</span></span>

 <span data-ttu-id="6e01e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6e01e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6e01e-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6e01e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6e01e-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="6e01e-109">_lpMessage_</span></span>
  
> <span data-ttu-id="6e01e-110">no Um ponteiro para um objeto Message (representando a mensagem de entrada) que tem permissão de leitura/gravação, que é usada pelo provedor de transporte para acessar e manipular essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e01e-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="6e01e-111">Este objeto permanece válido até que o provedor de transporte retorne da chamada para **IXPLogon:: StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="6e01e-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="6e01e-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="6e01e-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="6e01e-113">bota Um ponteiro para um valor de referência atribuído à mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e01e-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="6e01e-114">O spooler MAPI inicializa esse valor como 1 antes de retornar o ponteiro para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="6e01e-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e01e-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6e01e-115">Return value</span></span>

<span data-ttu-id="6e01e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e01e-116">S_OK</span></span> 
  
> <span data-ttu-id="6e01e-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="6e01e-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e01e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e01e-118">Remarks</span></span>

<span data-ttu-id="6e01e-119">O spooler MAPI chama o método **IXPLogon:: StartMessage** para iniciar a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e01e-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="6e01e-120">Antes de o provedor de transporte começar a usar a mensagem indicada pelo _lpMessage_, ele deve armazenar uma referência de mensagem no parâmetro _lpulMsgRef_ para uso potencial por uma chamada para o método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="6e01e-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="6e01e-121">Durante uma chamada **StartMessage** , o spooler MAPI processa os métodos para objetos abertos durante a transferência da mensagem e também processa qualquer anexo.</span><span class="sxs-lookup"><span data-stu-id="6e01e-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="6e01e-122">Esse processamento pode levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="6e01e-122">This processing can take a long time.</span></span> <span data-ttu-id="6e01e-123">Os provedores de transporte podem chamar a função de retorno de chamada [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) para o spooler MAPI com frequência durante esse processamento para liberar o tempo de CPU para outras tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="6e01e-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="6e01e-124">Todos os destinatários na tabela de destinatários que o provedor de transporte cria para a mensagem devem conter todas as propriedades de endereçamento necessárias.</span><span class="sxs-lookup"><span data-stu-id="6e01e-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="6e01e-125">Se necessário, o provedor pode construir um destinatário personalizado para representar um determinado destinatário.</span><span class="sxs-lookup"><span data-stu-id="6e01e-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="6e01e-126">No enTanto, se o provedor puder produzir uma entrada de destinatário que inclua mais informações, ele deverá fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6e01e-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="6e01e-127">Por exemplo, se um provedor de transporte tiver informações suficientes sobre o formato de destinatário de um provedor de catálogo de endereços que possa criar um identificador de entrada válido para um destinatário desse formato, ele deverá criar o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e01e-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="6e01e-128">Se qualquer propriedade não-transmittable for recebida, o provedor de transporte não deverá armazená-las na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e01e-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="6e01e-129">No enTanto, o provedor de transporte deve armazenar todas as propriedades de transmittable recebidas na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e01e-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="6e01e-130">Se a mensagem de entrada for um relatório de entrega ou um relatório de não entrega e o provedor de transporte não puder usar o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para gerar o relatório a partir da mensagem original, o provedor deverá preencher a mensagem com as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6e01e-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="6e01e-131">No enTanto, o provedor de transporte não pode definir a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e01e-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6e01e-132">Para salvar a mensagem de entrada no repositório de mensagens MAPI apropriado após o processamento, o provedor de transporte chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="6e01e-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="6e01e-133">Se o provedor de transporte não tiver nenhuma mensagem para passar para o spooler MAPI, ele poderá interromper a mensagem de entrada retornando da chamada **StartMessage** sem chamar **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="6e01e-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="6e01e-134">Todos os objetos que o provedor de transporte abre durante uma chamada de **StartMessage** devem ser liberados antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="6e01e-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="6e01e-135">No enTanto, o provedor não deve liberar o objeto Message que o spooler MAPI aprovou originalmente no parâmetro _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="6e01e-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="6e01e-136">Se **StartMessage** retornar um erro, a mensagem em processo será lançada sem que as alterações sejam salvas e perdidas.</span><span class="sxs-lookup"><span data-stu-id="6e01e-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="6e01e-137">Nesse caso, o provedor de transporte deve passar o sinalizador NOTIFY_CRITICAL_ERROR com uma chamada para o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) e chamar o método [IXPLogon::P oll](ixplogon-poll.md) para NOTIFICAr o spooler MAPI de que ele está em uma condição de erro grave.</span><span class="sxs-lookup"><span data-stu-id="6e01e-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="6e01e-138">Para obter mais informações, consulte [interagindo com o spooler MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="6e01e-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e01e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e01e-139">See also</span></span>



[<span data-ttu-id="6e01e-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6e01e-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="6e01e-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="6e01e-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="6e01e-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="6e01e-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="6e01e-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="6e01e-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="6e01e-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="6e01e-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="6e01e-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="6e01e-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="6e01e-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="6e01e-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="6e01e-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e01e-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

