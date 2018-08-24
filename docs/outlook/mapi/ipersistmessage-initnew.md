---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: efeac5a54c576d8b76d94ea7af8949e64dbccab6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588507"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="67df5-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="67df5-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="67df5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67df5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67df5-105">Inicializa uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="67df5-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="67df5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67df5-106">Parameters</span></span>

 <span data-ttu-id="67df5-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="67df5-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="67df5-108">[in] Um ponteiro para o site de mensagem que o formulário usará para trabalhar com a mensagem no visualizador.</span><span class="sxs-lookup"><span data-stu-id="67df5-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="67df5-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="67df5-109">_pMessage_</span></span>
  
> <span data-ttu-id="67df5-110">[in] Um ponteiro para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="67df5-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67df5-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="67df5-111">Return value</span></span>

<span data-ttu-id="67df5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="67df5-112">S_OK</span></span> 
  
> <span data-ttu-id="67df5-113">A nova mensagem foi inicializada com êxito.</span><span class="sxs-lookup"><span data-stu-id="67df5-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67df5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67df5-114">Remarks</span></span>

<span data-ttu-id="67df5-115">Visualizadores de formulário chame o método de **IPersistMessage::InitNew** quando o usuário escreve uma nova mensagem que pertence a uma classe de mensagem que processa o formulário.</span><span class="sxs-lookup"><span data-stu-id="67df5-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="67df5-116">Se o objeto de formulário tiver um ponteiro de interface de usuário válido, a interface do usuário para o objeto de mensagem deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="67df5-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="67df5-117">**InitNew** não deve ser chamado quando o formulário estiver em qualquer estado, exceto o estado [não inicializado](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="67df5-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="67df5-118">Se o formulário estiver em um dos outros estados quando **InitNew** é chamado, retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="67df5-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="67df5-119">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="67df5-119">Notes to implementers</span></span>

<span data-ttu-id="67df5-120">Normalmente, as mensagens que não foram salvas propriedades são marcadas como modificado para que o cliente pode exibir uma caixa de diálogo que solicita ao usuário se essas propriedades devem ser salvas.</span><span class="sxs-lookup"><span data-stu-id="67df5-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="67df5-121">Se o usuário indica que uma mensagem deve ser salvo, salvar os dados, marcar a mensagem como limpa e saia normalmente.</span><span class="sxs-lookup"><span data-stu-id="67df5-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="67df5-122">No entanto, se o processamento de suas mensagens recentemente inicializados inclui a definição de uma ou mais computado propriedades e é importante que essas propriedades a serem salvos, não marca as mensagens como modificado.</span><span class="sxs-lookup"><span data-stu-id="67df5-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="67df5-123">Porque computados propriedades devem ser visíveis aos usuários, nenhuma caixa de diálogo deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="67df5-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="67df5-124">Se o seu formulário tem uma referência a um site da mensagem ativa diferente daquela que é passado para **InitNew**, libere o site original porque ele não será usado.</span><span class="sxs-lookup"><span data-stu-id="67df5-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="67df5-125">Armazene os ponteiros para o site de mensagem e a mensagem de que os parâmetros _pMessageSite_ e _pMessage_ e chamar métodos de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos objetos para incrementar seus contagens de referência.</span><span class="sxs-lookup"><span data-stu-id="67df5-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="67df5-126">Defina as propriedades de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da nova mensagem e o **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para algo apropriado para sua classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="67df5-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="67df5-127">Muitas classes de mensagem, por exemplo, defina **PR_MESSAGE_FLAGS** como MSGFLAG_UNSENT para novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="67df5-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="67df5-128">Antes de retornar, a transição do formulário para o estado [Normal](normal-state.md) , se nenhum erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="67df5-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="67df5-129">Enviar uma notificação de mensagem nova para todos os visualizadores registrados chamando os métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="67df5-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="67df5-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="67df5-130">Notes to callers</span></span>

<span data-ttu-id="67df5-131">Depois de fazer uma chamada bem sucedida a **InitNew**, você pode assumir que as seguintes propriedades necessárias e nenhum outro foram definidos para o formulário:</span><span class="sxs-lookup"><span data-stu-id="67df5-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="67df5-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="67df5-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="67df5-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="67df5-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="67df5-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="67df5-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="67df5-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67df5-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="67df5-139">Para obter mais informações sobre os estados de formulários, consulte [Estados de formulário](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="67df5-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="67df5-140">Para obter mais informações sobre como os objetos de armazenamento são inicializados, consulte o método [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="67df5-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67df5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="67df5-141">See also</span></span>



[<span data-ttu-id="67df5-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67df5-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

