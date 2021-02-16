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
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437361"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="eca0e-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="eca0e-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="eca0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eca0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eca0e-105">Salva todas as propriedades da mensagem e marca a mensagem como pronta para ser enviada.</span><span class="sxs-lookup"><span data-stu-id="eca0e-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="eca0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eca0e-106">Parameters</span></span>

 <span data-ttu-id="eca0e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eca0e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="eca0e-108">[in] Bitmask de sinalizadores usados para controlar como uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="eca0e-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="eca0e-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="eca0e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="eca0e-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="eca0e-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="eca0e-111">O MAPI deve enviar a mensagem imediatamente.</span><span class="sxs-lookup"><span data-stu-id="eca0e-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="eca0e-112">Esse sinalizador não está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="eca0e-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eca0e-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eca0e-113">Return value</span></span>

<span data-ttu-id="eca0e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="eca0e-114">S_OK</span></span> 
  
> <span data-ttu-id="eca0e-115">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="eca0e-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eca0e-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="eca0e-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="eca0e-117">A tabela de destinatários da mensagem está vazia.</span><span class="sxs-lookup"><span data-stu-id="eca0e-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eca0e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eca0e-118">Remarks</span></span>

<span data-ttu-id="eca0e-119">O **método IMessage::SubmitMessage** marca uma mensagem como pronta para ser transmitida.</span><span class="sxs-lookup"><span data-stu-id="eca0e-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="eca0e-120">O MAPI passa mensagens para o sistema de mensagens subjacente na ordem em que são marcadas para envio.</span><span class="sxs-lookup"><span data-stu-id="eca0e-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="eca0e-121">Devido a essa funcionalidade, uma mensagem pode permanecer em um armazenamento de mensagens por algum tempo antes que o sistema de mensagens subjacente possa assumir a responsabilidade por ela.</span><span class="sxs-lookup"><span data-stu-id="eca0e-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="eca0e-122">A ordem de recebimento no destino está no controle do sistema de mensagens subjacente e não necessariamente corresponder à ordem na qual as mensagens foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="eca0e-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eca0e-123">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="eca0e-123">Notes to implementers</span></span>

<span data-ttu-id="eca0e-124">Chame o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvá-la e verifique a propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="eca0e-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="eca0e-125">Se o MSGFLAG_RESEND sinalizador estiver definido, chame [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="eca0e-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="eca0e-126">**PrepareSubmit** atualiza o tipo de destinatário **e** PR_RESPONSIBILITY ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos os destinatários na mensagem de reemissão.</span><span class="sxs-lookup"><span data-stu-id="eca0e-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="eca0e-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="eca0e-127">Notes to callers</span></span>

<span data-ttu-id="eca0e-128">Quando **SubmitMessage** retorna, todos os ponteiros para a mensagem e suas mensagens, pastas, anexos, fluxos, tabelas e assim por diante associados não são mais válidos.</span><span class="sxs-lookup"><span data-stu-id="eca0e-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="eca0e-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span><span class="sxs-lookup"><span data-stu-id="eca0e-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="eca0e-130">O MAPI foi projetado de forma que, depois **que SubmitMessage** for chamado, você deverá liberar a mensagem e todos os subobjetos associados.</span><span class="sxs-lookup"><span data-stu-id="eca0e-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="eca0e-131">No entanto, se **SubmitMessage** retornar um valor de erro indicando informações ausentes ou inválidas, a mensagem permanecerá aberta e os ponteiros permanecerão válidos.</span><span class="sxs-lookup"><span data-stu-id="eca0e-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="eca0e-132">Para cancelar uma operação de envio, obter e armazenar um ponteiro para a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem antes de a mensagem ser enviada.</span><span class="sxs-lookup"><span data-stu-id="eca0e-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="eca0e-133">Como o identificador de entrada de uma mensagem é invalidado após o envio da mensagem, é necessário salvá-la antes de chamar **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="eca0e-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="eca0e-134">Para cancelar o envio, aponte o parâmetro  _lpEntryId_ para esse identificador de entrada e chame [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="eca0e-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eca0e-135">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="eca0e-135">MFCMAPI reference</span></span>

<span data-ttu-id="eca0e-136">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eca0e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eca0e-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="eca0e-137">**File**</span></span>|<span data-ttu-id="eca0e-138">**Função**</span><span class="sxs-lookup"><span data-stu-id="eca0e-138">**Function**</span></span>|<span data-ttu-id="eca0e-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="eca0e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eca0e-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="eca0e-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="eca0e-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="eca0e-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="eca0e-142">MFCMAPI usa o **método IMessage::SubmitMessage** para enviar a mensagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="eca0e-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eca0e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="eca0e-143">See also</span></span>



[<span data-ttu-id="eca0e-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="eca0e-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="eca0e-145">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eca0e-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="eca0e-146">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="eca0e-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

