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
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="c7ec9-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="c7ec9-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="c7ec9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7ec9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7ec9-105">Indica se o formulário pode manipular a classe de mensagem da próxima mensagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="c7ec9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7ec9-106">Parameters</span></span>

 <span data-ttu-id="c7ec9-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="c7ec9-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="c7ec9-108">[in] Um ponteiro para a classe de mensagem da próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="c7ec9-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="c7ec9-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="c7ec9-110">[in] Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor, copiada da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da próxima mensagem a ser exibida, que fornece informações de status relacionadas ao índice de conteúdo em que a mensagem está incluída.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="c7ec9-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="c7ec9-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="c7ec9-112">[in] Um ponteiro para uma máscara de bits de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da próxima mensagem a ser exibida que indica o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="c7ec9-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="c7ec9-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="c7ec9-114">[out] Um ponteiro para um ponteiro para a implementação [de IPersistMessage](ipersistmessageiunknown.md) para o objeto de formulário usado para o novo formulário, se um novo formulário for necessário.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="c7ec9-115">Um ponteiro para NULL poderá ser retornado se o objeto de formulário atual puder ser usado para exibir e salvar a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7ec9-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c7ec9-116">Return value</span></span>

<span data-ttu-id="c7ec9-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7ec9-117">S_OK</span></span> 
  
> <span data-ttu-id="c7ec9-118">A notificação foi bem-sucedida e o formulário pode manipular a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="c7ec9-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c7ec9-119">S_FALSE</span></span> 
  
> <span data-ttu-id="c7ec9-120">O formulário não trata a classe de mensagem da próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7ec9-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ec9-121">Remarks</span></span>

<span data-ttu-id="c7ec9-122">Visualizadores de formulário chamam o método **IMAPIFormAdviseSink::OnActivateNext** para ajudar o formulário a determinar se ele pode exibir a próxima mensagem em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="c7ec9-123">A próxima mensagem pode ser uma mensagem de qualquer classe, mas normalmente é da mesma classe ou de uma classe relacionada.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="c7ec9-124">Isso torna o processo de leitura de várias mensagens da mesma classe mais eficiente, permitindo que os aplicativos clientes reutilizar objetos de formulário sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="c7ec9-125">A maioria dos objetos de formulário usará a classe de mensagem apontada pelo parâmetro  _lpszMessageClass_ para determinar se eles podem manipular a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="c7ec9-126">Normalmente, um formulário pode manipular mensagens que pertencem a classes das quais a classe padrão do formulário é uma subclasse, além de mensagens que pertencem à classe padrão.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="c7ec9-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c7ec9-128">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="c7ec9-128">Notes to implementers</span></span>

<span data-ttu-id="c7ec9-129">Retornar S_OK e NULL no  _parâmetro ppPersistMessage_ se o formulário puder manipular a classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="c7ec9-130">Se o formulário puder criar um novo formulário que possa manipular a mensagem que o formulário não pode manipular, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="c7ec9-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="c7ec9-131">Chame a fábrica de classe do formulário para criar uma instância de um novo objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="c7ec9-132">Armazene essa instância no conteúdo do parâmetro _de ponteiro ppPersistMessage._</span><span class="sxs-lookup"><span data-stu-id="c7ec9-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="c7ec9-133">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-133">Return S_OK.</span></span>
    
<span data-ttu-id="c7ec9-134">O visualizador de formulário carregará a mensagem usando o método [IPersistMessage::Load](ipersistmessage-load.md) que pertence ao objeto apontado pelo  _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="c7ec9-135">Se nem o formulário nem um formulário que você pode criar podem manipular a próxima mensagem, retorne S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="c7ec9-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c7ec9-137">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c7ec9-137">MFCMAPI reference</span></span>

<span data-ttu-id="c7ec9-138">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7ec9-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c7ec9-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c7ec9-139">**File**</span></span>|<span data-ttu-id="c7ec9-140">**Função**</span><span class="sxs-lookup"><span data-stu-id="c7ec9-140">**Function**</span></span>|<span data-ttu-id="c7ec9-141">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="c7ec9-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7ec9-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c7ec9-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c7ec9-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="c7ec9-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="c7ec9-144">MFCMAPI usa o método **IMAPIFormAdviseSink::OnActivateNext** para implementar o método [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)</span><span class="sxs-lookup"><span data-stu-id="c7ec9-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7ec9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7ec9-145">See also</span></span>



[<span data-ttu-id="c7ec9-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="c7ec9-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="c7ec9-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7ec9-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="c7ec9-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="c7ec9-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="c7ec9-149">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="c7ec9-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="c7ec9-150">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c7ec9-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="c7ec9-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7ec9-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="c7ec9-152">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c7ec9-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

