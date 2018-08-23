---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 67c86f39898b4bd0c019b9b3095c9449e6e60b1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567318"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="cf6e9-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cf6e9-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="cf6e9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf6e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf6e9-105">Salva todas as propriedades da mensagem e marca a mensagem como pronta para ser enviada.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf6e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf6e9-106">Parameters</span></span>

 <span data-ttu-id="cf6e9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf6e9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cf6e9-108">[in] Bitmask dos sinalizadores usadas para controlar como uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="cf6e9-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="cf6e9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="cf6e9-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="cf6e9-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="cf6e9-111">MAPI deve enviar a mensagem imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="cf6e9-112">Esse sinalizador não está atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf6e9-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cf6e9-113">Return value</span></span>

<span data-ttu-id="cf6e9-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf6e9-114">S_OK</span></span> 
  
> <span data-ttu-id="cf6e9-115">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cf6e9-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="cf6e9-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="cf6e9-117">Tabela de destinatário da mensagem está vazia.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf6e9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf6e9-118">Remarks</span></span>

<span data-ttu-id="cf6e9-119">O método **IMessage::SubmitMessage** marca uma mensagem como pronto para ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="cf6e9-120">MAPI passa mensagens para o sistema de mensagens subjacente na ordem em que estão marcados para envio.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="cf6e9-121">Devido a essa funcionalidade, uma mensagem pode ficar em um armazenamento de mensagens, por algum tempo antes que o sistema de mensagens subjacente pode assumir a responsabilidade para ele.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="cf6e9-122">A ordem de recebimento no destino está no controle do sistema de mensagens subjacentes e não necessariamente correspondem a ordem na qual as mensagens foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cf6e9-123">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="cf6e9-123">Notes to implementers</span></span>

<span data-ttu-id="cf6e9-124">Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvá-lo e, em seguida, verifique a propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="cf6e9-125">Se o sinalizador MSGFLAG_RESEND estiver definido, chame [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="cf6e9-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="cf6e9-126">**PrepareSubmit** atualiza o tipo de destinatário e a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos os destinatários da mensagem de reenvio.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf6e9-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="cf6e9-127">Notes to callers</span></span>

<span data-ttu-id="cf6e9-128">Quando **SubmitMessage** retorna, todos os ponteiros para a mensagem e suas mensagens associadas subobjetos, pastas, anexos, fluxos, tabelas e assim por diante não estão mais válidos.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="cf6e9-129">MAPI não permite que quaisquer operações mais sobre esses ponteiros, exceto para chamar seus métodos **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="cf6e9-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="cf6e9-130">MAPI destina-se a forma que depois é chamado **SubmitMessage** , você deve liberar a mensagem e todos os respectivos subobjetos.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="cf6e9-131">No entanto, se **SubmitMessage** retorna um valor de erro indicando informações ausentes ou inválidas, a mensagem permanecerá aberta e os ponteiros permanecem válidos.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="cf6e9-132">Para cancelar uma operação de envio, obtenha e armazenar um ponteiro para a propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem antes que a mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="cf6e9-133">Porque o identificador de entrada da mensagem é invalidado depois que a mensagem foi enviada, é necessário para salvá-lo antes de chamar **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="cf6e9-134">Para cancelar a enviar, aponte o parâmetro _lpEntryId_ para esse identificador de entrada e chamadas [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="cf6e9-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf6e9-135">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cf6e9-135">MFCMAPI reference</span></span>

<span data-ttu-id="cf6e9-136">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf6e9-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="cf6e9-137">**File**</span></span>|<span data-ttu-id="cf6e9-138">**Function**</span><span class="sxs-lookup"><span data-stu-id="cf6e9-138">**Function**</span></span>|<span data-ttu-id="cf6e9-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cf6e9-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf6e9-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cf6e9-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="cf6e9-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="cf6e9-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="cf6e9-142">MFCMAPI usa o método **IMessage::SubmitMessage** para enviar a mensagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="cf6e9-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf6e9-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf6e9-143">See also</span></span>



[<span data-ttu-id="cf6e9-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="cf6e9-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="cf6e9-145">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cf6e9-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="cf6e9-146">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="cf6e9-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

