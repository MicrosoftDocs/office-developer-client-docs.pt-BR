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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d9235da7e7ec6ec244ee1a75f4795e9c77ec28bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579946"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="50410-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="50410-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="50410-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50410-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50410-105">Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="50410-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="50410-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50410-106">Parameters</span></span>

 <span data-ttu-id="50410-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50410-107">_ulFlags_</span></span>
  
> <span data-ttu-id="50410-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="50410-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="50410-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="50410-109">_lpMessage_</span></span>
  
> <span data-ttu-id="50410-110">[in] Um ponteiro para um objeto de mensagem (representando a mensagem de entrada) que tem permissão de leitura/gravação, que é usado pelo provedor de transporte para acessar e manipular a mensagem.</span><span class="sxs-lookup"><span data-stu-id="50410-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="50410-111">Este objeto permanecerá válido até depois que o provedor de transporte retornará da chamada para **IXPLogon::StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="50410-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="50410-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="50410-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="50410-113">[out] Um ponteiro para um valor de referência atribuído à mensagem.</span><span class="sxs-lookup"><span data-stu-id="50410-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="50410-114">O MAPI spooler inicializa esse valor como 1 antes que ele retorna o ponteiro para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="50410-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50410-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="50410-115">Return value</span></span>

<span data-ttu-id="50410-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="50410-116">S_OK</span></span> 
  
> <span data-ttu-id="50410-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="50410-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50410-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="50410-118">Remarks</span></span>

<span data-ttu-id="50410-119">O MAPI spooler chama o método **IXPLogon::StartMessage** para iniciar a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="50410-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="50410-120">Antes do provedor de transporte começa a usar a mensagem apontada pela _lpMessage_, ele deve armazenar uma referência de mensagem no parâmetro _lpulMsgRef_ para uso potencial por uma chamada ao método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="50410-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="50410-121">Durante uma chamada de **StartMessage** , o MAPI spooler processa métodos para objetos abertos durante a transferência da mensagem, e também processa todos os anexos.</span><span class="sxs-lookup"><span data-stu-id="50410-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="50410-122">Esse processamento pode levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="50410-122">This processing can take a long time.</span></span> <span data-ttu-id="50410-123">Provedores de transporte podem chamar a função de retorno de chamada [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o MAPI spooler frequentemente durante o processamento para liberar o tempo da CPU para outras tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="50410-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="50410-124">Todos os destinatários na tabela de destinatário que cria um provedor de transporte para a mensagem devem conter todas as propriedades obrigatórias de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="50410-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="50410-125">Se necessário, o provedor pode construir um destinatário personalizado para representar um destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="50410-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="50410-126">No entanto, se o provedor pode gerar uma entrada do destinatário que inclui mais informações, ele deve fazer isso.</span><span class="sxs-lookup"><span data-stu-id="50410-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="50410-127">Por exemplo, se um provedor de transporte tem informações suficientes sobre formato de destinatário de um provedor catálogo de endereços que ele pode construir um identificador de entrada válida para um destinatário para esse formato, ele deve construir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="50410-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="50410-128">Se todas as propriedades nontransmittable são recebidas, o provedor de transporte não deve armazená-los na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="50410-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="50410-129">No entanto, o provedor de transporte deve armazenar todas as propriedades transmittable, que ele recebe na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="50410-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="50410-130">Se a mensagem de entrada é um relatório de entrega ou um relatório de não entrega e o provedor de transporte é possível utilizar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para gerar o relatório a partir da mensagem original, o provedor, em si, deve popular a mensagem com as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="50410-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="50410-131">No entanto, o provedor de transporte não pode definir a propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="50410-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="50410-132">Para salvar a mensagem de entrada no armazenamento de mensagens MAPI apropriado após o processamento, o provedor de transporte chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="50410-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="50410-133">Se o provedor de transporte não tem todas as mensagens a serem passados para o spooler MAPI, ele pode interromper a mensagem de entrada, retornando da chamada **StartMessage** sem chamar **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="50410-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="50410-134">Todos os objetos que o provedor de transporte abre durante uma chamada de **StartMessage** devem ser liberados antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="50410-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="50410-135">No entanto, o provedor não deve liberar o objeto de mensagem que o MAPI spooler originalmente passado no parâmetro _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="50410-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="50410-136">Se **StartMessage** retornará um erro, a mensagem no processo for lançada sem ter que as alterações foram salvas e serão perdida.</span><span class="sxs-lookup"><span data-stu-id="50410-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="50410-137">Nesse caso, o provedor de transporte deve passar o sinalizador NOTIFY_CRITICAL_ERROR com uma chamada para o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) e chame o método [IXPLogon::Poll](ixplogon-poll.md) para notificar o MAPI spooler que ele está em uma condição de erro grave.</span><span class="sxs-lookup"><span data-stu-id="50410-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="50410-138">Para obter mais informações, consulte [interagindo com o Spooler de MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="50410-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50410-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="50410-139">See also</span></span>



[<span data-ttu-id="50410-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="50410-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="50410-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="50410-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="50410-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="50410-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="50410-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="50410-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="50410-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="50410-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="50410-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="50410-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="50410-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="50410-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="50410-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50410-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

