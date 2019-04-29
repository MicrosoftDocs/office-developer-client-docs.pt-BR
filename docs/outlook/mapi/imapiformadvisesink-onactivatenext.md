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
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411761"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="ca50e-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="ca50e-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="ca50e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca50e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca50e-105">Indica se o formulário pode manipular a classe de mensagem da próxima mensagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="ca50e-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ca50e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca50e-106">Parameters</span></span>

 <span data-ttu-id="ca50e-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ca50e-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="ca50e-108">no Um ponteiro para a classe de mensagem da próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca50e-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="ca50e-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="ca50e-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="ca50e-110">no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor, copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da próxima mensagem a ser exibida, que fornece informações de status sobre a tabela de conteúdo que a mensagem está incluída no.</span><span class="sxs-lookup"><span data-stu-id="ca50e-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="ca50e-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="ca50e-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="ca50e-112">no Um ponteiro para uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da próxima mensagem a ser exibida, indicando o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca50e-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="ca50e-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="ca50e-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="ca50e-114">bota Um ponteiro para um ponteiro para a implementação do [IPersistMessage](ipersistmessageiunknown.md) do objeto Form usado para o novo formulário, se um novo formulário for necessário.</span><span class="sxs-lookup"><span data-stu-id="ca50e-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="ca50e-115">Um ponteiro para nulo pode ser retornado se o objeto Form atual puder ser usado para exibir e salvar a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca50e-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca50e-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca50e-116">Return value</span></span>

<span data-ttu-id="ca50e-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca50e-117">S_OK</span></span> 
  
> <span data-ttu-id="ca50e-118">A notificação foi bem-sucedida e o formulário pode lidar com a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca50e-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="ca50e-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ca50e-119">S_FALSE</span></span> 
  
> <span data-ttu-id="ca50e-120">O formulário não manipula a classe de mensagem da mensagem seguinte.</span><span class="sxs-lookup"><span data-stu-id="ca50e-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca50e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca50e-121">Remarks</span></span>

<span data-ttu-id="ca50e-122">Os visualizadores de formulários chamam o método **IMAPIFormAdviseSink:: OnActivateNext** para ajudar o formulário a determinar se pode exibir a próxima mensagem em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="ca50e-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="ca50e-123">A próxima mensagem pode ser uma mensagem de qualquer classe, mas geralmente é da mesma classe ou de uma classe relacionada.</span><span class="sxs-lookup"><span data-stu-id="ca50e-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="ca50e-124">Isso torna mais eficiente o processo de leitura de várias mensagens da mesma classe, permitindo que os aplicativos cliente reutilizem objetos de formulário sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="ca50e-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="ca50e-125">A maioria dos objetos de formulário usará a classe de mensagem apontada pelo parâmetro _lpszMessageClass_ para determinar se eles podem manipular a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca50e-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="ca50e-126">Geralmente, um formulário pode lidar com mensagens que pertencem a classes das quais a classe padrão do formulário é uma subclasse, além de mensagens que pertencem à classe padrão.</span><span class="sxs-lookup"><span data-stu-id="ca50e-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="ca50e-127">No enTanto, um formulário pode usar outros fatores para determinar sem dúvida se uma mensagem pode ser tratada, como o status enviado ou não enviado da mensagem seguinte.</span><span class="sxs-lookup"><span data-stu-id="ca50e-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ca50e-128">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ca50e-128">Notes to implementers</span></span>

<span data-ttu-id="ca50e-129">Retornar S_OK e NULL no parâmetro _ppPersistMessage_ se o formulário puder manipular a classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca50e-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="ca50e-130">Se o formulário puder criar um novo formulário que possa lidar com a mensagem de que o formulário não pode lidar, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="ca50e-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="ca50e-131">Chame o alocador de classe do formulário para criar uma instância de um novo objeto Form.</span><span class="sxs-lookup"><span data-stu-id="ca50e-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="ca50e-132">Armazene essa instância no conteúdo do parâmetro de ponteiro _ppPersistMessage_ .</span><span class="sxs-lookup"><span data-stu-id="ca50e-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="ca50e-133">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="ca50e-133">Return S_OK.</span></span>
    
<span data-ttu-id="ca50e-134">O Visualizador de formulários carregará a mensagem usando o método [IPersistMessage:: Load](ipersistmessage-load.md) que pertence ao objeto apontado por _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="ca50e-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="ca50e-135">Se nem o formulário nem um formulário que você pode criar podem manipular a próxima mensagem, retorne S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="ca50e-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="ca50e-136">No enTanto, em geral, os formulários não devem retornar esse valor porque causa uma redução no desempenho no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="ca50e-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ca50e-137">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ca50e-137">MFCMAPI reference</span></span>

<span data-ttu-id="ca50e-138">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca50e-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ca50e-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ca50e-139">**File**</span></span>|<span data-ttu-id="ca50e-140">**Função**</span><span class="sxs-lookup"><span data-stu-id="ca50e-140">**Function**</span></span>|<span data-ttu-id="ca50e-141">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ca50e-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca50e-142">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="ca50e-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ca50e-143">CMyMAPIFormViewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ca50e-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="ca50e-144">MFCMAPI usa o método **IMAPIFormAdviseSink:: OnActivateNext** para implementar o método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="ca50e-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca50e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca50e-145">See also</span></span>



[<span data-ttu-id="ca50e-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ca50e-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="ca50e-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca50e-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="ca50e-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="ca50e-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="ca50e-149">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="ca50e-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="ca50e-150">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ca50e-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="ca50e-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca50e-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="ca50e-152">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ca50e-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

