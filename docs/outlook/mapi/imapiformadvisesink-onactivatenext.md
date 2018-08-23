---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e8fb69e7d25420186d7269943c5d957311e813d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581752"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="018b7-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="018b7-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="018b7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="018b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="018b7-105">Indica se o formulário pode lidar com a classe de mensagem da próxima mensagem para exibir.</span><span class="sxs-lookup"><span data-stu-id="018b7-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="018b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="018b7-106">Parameters</span></span>

 <span data-ttu-id="018b7-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="018b7-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="018b7-108">[in] Um ponteiro para a classe de mensagem da próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="018b7-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="018b7-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="018b7-110">[in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente, copiado da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem próxima a exibir, que fornece informações de status sobre a tabela de conteúdo que a mensagem é incluída in.</span><span class="sxs-lookup"><span data-stu-id="018b7-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="018b7-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="018b7-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="018b7-112">[in] Um ponteiro para uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem próxima a exibir que indica o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="018b7-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="018b7-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="018b7-114">[out] Um ponteiro para um ponteiro para a implementação de [IPersistMessage](ipersistmessageiunknown.md) para o objeto de formulário usado para o novo formulário, se um novo formulário é necessário.</span><span class="sxs-lookup"><span data-stu-id="018b7-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="018b7-115">Um ponteiro como NULL pode ser retornado se o objeto atual do formulário pode ser usado para exibir e salvar a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="018b7-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="018b7-116">Return value</span></span>

<span data-ttu-id="018b7-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="018b7-117">S_OK</span></span> 
  
> <span data-ttu-id="018b7-118">A notificação foi bem-sucedida e o formulário pode manipular a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="018b7-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="018b7-119">S_FALSE</span></span> 
  
> <span data-ttu-id="018b7-120">O formulário não processa a classe de mensagem da próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="018b7-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="018b7-121">Remarks</span></span>

<span data-ttu-id="018b7-122">Visualizadores de formulário chame o método de **IMAPIFormAdviseSink::OnActivateNext** para ajudar a determinar se ele pode exibir a próxima mensagem em uma pasta de formulário.</span><span class="sxs-lookup"><span data-stu-id="018b7-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="018b7-123">A próxima mensagem poderia ser uma mensagem de qualquer classe, mas geralmente é da mesma classe ou uma classe relacionada.</span><span class="sxs-lookup"><span data-stu-id="018b7-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="018b7-124">Isso faz com que o processo de leitura várias mensagens da mesma classe mais eficiente, permitindo que aplicativos de cliente reutilizar os objetos de formulário sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="018b7-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="018b7-125">A maioria dos objetos do formulário usará a classe de mensagem apontada pelo parâmetro _lpszMessageClass_ para determinar se podem lidar com a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="018b7-126">Geralmente, um formulário pode manipular mensagens que pertencem às classes do qual a classe do formulário padrão é uma subclasse, além das mensagens que pertencem à classe padrão.</span><span class="sxs-lookup"><span data-stu-id="018b7-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="018b7-127">No entanto, um formulário pode usar outros fatores para determinar sem pergunta se uma mensagem pode ser lida, como o status enviado ou não enviado da próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="018b7-128">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="018b7-128">Notes to implementers</span></span>

<span data-ttu-id="018b7-129">Retorne S_OK e NULL no parâmetro _ppPersistMessage_ se o formulário pode manipular a classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="018b7-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="018b7-130">Se o formulário pode criar um novo formulário que pode manipular a mensagem que o formulário é capaz de manipular, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="018b7-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="018b7-131">Chame o alocador de classe do formulário para criar uma instância de um novo objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="018b7-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="018b7-132">Armazene essa instância no conteúdo do parâmetro _ppPersistMessage_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="018b7-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="018b7-133">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="018b7-133">Return S_OK.</span></span>
    
<span data-ttu-id="018b7-134">A tela de formulário será carregado a mensagem usando o método [IPersistMessage::Load](ipersistmessage-load.md) que pertence ao objeto apontado pela _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="018b7-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="018b7-135">Se nem o formulário nem em um formulário que você pode criar pode manipular a próxima mensagem, retorne S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="018b7-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="018b7-136">No entanto, em geral, formulários não devem retornar que esse valor porque isso causar redução de desempenho no Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="018b7-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="018b7-137">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="018b7-137">MFCMAPI reference</span></span>

<span data-ttu-id="018b7-138">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="018b7-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="018b7-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="018b7-139">**File**</span></span>|<span data-ttu-id="018b7-140">**Function**</span><span class="sxs-lookup"><span data-stu-id="018b7-140">**Function**</span></span>|<span data-ttu-id="018b7-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="018b7-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="018b7-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="018b7-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="018b7-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="018b7-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="018b7-144">MFCMAPI usa o método **IMAPIFormAdviseSink::OnActivateNext** para implementar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="018b7-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="018b7-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="018b7-145">See also</span></span>



[<span data-ttu-id="018b7-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="018b7-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="018b7-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="018b7-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="018b7-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="018b7-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="018b7-149">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="018b7-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="018b7-150">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="018b7-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="018b7-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="018b7-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="018b7-152">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="018b7-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

