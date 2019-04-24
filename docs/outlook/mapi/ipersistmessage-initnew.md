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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317147"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="54bdd-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="54bdd-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="54bdd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54bdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54bdd-105">Inicializa uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="54bdd-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="54bdd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54bdd-106">Parameters</span></span>

 <span data-ttu-id="54bdd-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="54bdd-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="54bdd-108">no Um ponteiro para o site de mensagens que o formulário usará para trabalhar com a mensagem no visualizador.</span><span class="sxs-lookup"><span data-stu-id="54bdd-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="54bdd-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="54bdd-109">_pMessage_</span></span>
  
> <span data-ttu-id="54bdd-110">no Um ponteiro para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="54bdd-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54bdd-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="54bdd-111">Return value</span></span>

<span data-ttu-id="54bdd-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="54bdd-112">S_OK</span></span> 
  
> <span data-ttu-id="54bdd-113">A nova mensagem foi inicializada com êxito.</span><span class="sxs-lookup"><span data-stu-id="54bdd-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54bdd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="54bdd-114">Remarks</span></span>

<span data-ttu-id="54bdd-115">Os visualizadores de formulários chamam o método **IPersistMessage:: InitNew** quando o usuário grava uma nova mensagem que pertence a uma classe de mensagem que o formulário manipula.</span><span class="sxs-lookup"><span data-stu-id="54bdd-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="54bdd-116">Se o objeto Form tiver um ponteiro de interface do usuário válido, a interface do usuário para o objeto Message deverá ser exibida.</span><span class="sxs-lookup"><span data-stu-id="54bdd-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="54bdd-117">**InitNew** não deve ser chamado quando o formulário está em qualquer Estado, exceto [](uninitialized-state.md) o estado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="54bdd-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="54bdd-118">Se o formulário estiver em um dos outros Estados quando **InitNew** for chamado, retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="54bdd-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="54bdd-119">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="54bdd-119">Notes to implementers</span></span>

<span data-ttu-id="54bdd-120">Normalmente, as mensagens que têm propriedades não salvas são marcadas como modificadas para que o cliente possa exibir uma caixa de diálogo solicitando ao usuário se essas propriedades devem ser salvas.</span><span class="sxs-lookup"><span data-stu-id="54bdd-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="54bdd-121">Se o usuário indicar que uma mensagem deve ser salva, salve os dados, marque a mensagem como limpa e saia normalmente.</span><span class="sxs-lookup"><span data-stu-id="54bdd-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="54bdd-122">No enTanto, se o processamento de suas mensagens recentemente inicializadas incluir a configuração de uma ou mais propriedades computadas, e for importante que essas propriedades sejam salvas, não marque as mensagens como modificadas.</span><span class="sxs-lookup"><span data-stu-id="54bdd-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="54bdd-123">Como as propriedades computadas devem ser invisíveis aos usuários, nenhuma caixa de diálogo deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="54bdd-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="54bdd-124">Se o formulário tiver uma referência a um site de mensagem ativo diferente daquele que é passado no **InitNew**, libere o site original porque ele não será mais usado.</span><span class="sxs-lookup"><span data-stu-id="54bdd-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="54bdd-125">Armazene os ponteiros no site da mensagem e a mensagem dos parâmetros _pMessageSite_ e _PMessage_ e chame os métodos [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos dois objetos para incrementar suas contagens de referência.</span><span class="sxs-lookup"><span data-stu-id="54bdd-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="54bdd-126">Defina as propriedades **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para a nova mensagem para algo apropriado para sua classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="54bdd-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="54bdd-127">Muitas classes de mensagens, por exemplo, define **PR_MESSAGE_FLAGS** como MSGFLAG_UNSENT para novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="54bdd-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="54bdd-128">Antes de retornar, migre o formulário para o estado [normal](normal-state.md) se nenhum erro tiver ocorrido.</span><span class="sxs-lookup"><span data-stu-id="54bdd-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="54bdd-129">Envie uma nova notificação de mensagem para todos os visualizadores registrados chamando seus métodos [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="54bdd-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="54bdd-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="54bdd-130">Notes to callers</span></span>

<span data-ttu-id="54bdd-131">Depois de fazer uma chamada bem-sucedida para o **InitNew**, você pode supor que as seguintes propriedades obrigatórias e nenhuma outra tenham sido definidas para o formulário:</span><span class="sxs-lookup"><span data-stu-id="54bdd-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="54bdd-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="54bdd-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="54bdd-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="54bdd-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="54bdd-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="54bdd-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="54bdd-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54bdd-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="54bdd-139">Para obter mais informações sobre os Estados dos formulários, confira [Estados de formulário](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="54bdd-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="54bdd-140">Para obter mais informações sobre como os objetos de armazenamento são inicializados, consulte o método [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="54bdd-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54bdd-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="54bdd-141">See also</span></span>



[<span data-ttu-id="54bdd-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54bdd-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

