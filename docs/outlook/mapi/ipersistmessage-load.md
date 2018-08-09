---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767606"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="d8f92-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="d8f92-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="d8f92-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8f92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8f92-105">Carrega o formulário para uma mensagem especificada.</span><span class="sxs-lookup"><span data-stu-id="d8f92-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d8f92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8f92-106">Parameters</span></span>

 <span data-ttu-id="d8f92-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="d8f92-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="d8f92-108">[in] Um ponteiro para o site de mensagem para o formulário a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="d8f92-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="d8f92-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="d8f92-109">_pMessage_</span></span>
  
> <span data-ttu-id="d8f92-110">[in] Um ponteiro para a mensagem para o qual o formulário deve ser carregado.</span><span class="sxs-lookup"><span data-stu-id="d8f92-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="d8f92-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="d8f92-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="d8f92-112">[in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente, copiado de propriedade de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem, que fornecem informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d8f92-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="d8f92-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="d8f92-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="d8f92-114">[in] Uma bitmask dos sinalizadores, copiado de propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem, que fornecem mais informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d8f92-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8f92-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d8f92-115">Return value</span></span>

<span data-ttu-id="d8f92-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8f92-116">S_OK</span></span> 
  
> <span data-ttu-id="d8f92-117">O formulário foi carregado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d8f92-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8f92-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8f92-118">Remarks</span></span>

<span data-ttu-id="d8f92-119">Visualizadores de formulário chame o método de **IPersistMessage::Load** para carregar um formulário para uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="d8f92-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d8f92-120">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="d8f92-120">Notes to implementers</span></span>

 <span data-ttu-id="d8f92-121">**Carga** é chamado somente quando um formulário estiver em um dos seguintes estados:</span><span class="sxs-lookup"><span data-stu-id="d8f92-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="d8f92-122">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="d8f92-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="d8f92-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d8f92-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="d8f92-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="d8f92-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="d8f92-125">Se um visualizador de formulário chama **carga** enquanto o formulário está em qualquer outro estado, o método retornará E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d8f92-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="d8f92-126">Se o seu formulário tem uma referência a um site da mensagem ativa diferente daquela que é passado para o **carregamento**, libere o site original porque ele não será usado.</span><span class="sxs-lookup"><span data-stu-id="d8f92-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="d8f92-127">Armazene os ponteiros para o site de mensagem e a mensagem de que os parâmetros _pMessageSite_ e _pMessage_ e chamar métodos de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos objetos para incrementar seus contagens de referência.</span><span class="sxs-lookup"><span data-stu-id="d8f92-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="d8f92-128">Após **AddRef** , armazene as propriedades dos parâmetros _ulMessageStatus_ e _ulMessageFlags_ no formulário.</span><span class="sxs-lookup"><span data-stu-id="d8f92-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="d8f92-129">Fazer a transição de formulário ao seu estado [Normal](normal-state.md) antes de exibi-las e notificar os visualizadores registrados chamando os métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f92-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="d8f92-130">Se nenhum erro ocorrer, retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="d8f92-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8f92-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8f92-131">See also</span></span>



[<span data-ttu-id="d8f92-132">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="d8f92-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="d8f92-133">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="d8f92-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="d8f92-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8f92-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="d8f92-135">Estado Uninitialized</span><span class="sxs-lookup"><span data-stu-id="d8f92-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="d8f92-136">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d8f92-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="d8f92-137">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="d8f92-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="d8f92-138">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="d8f92-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="d8f92-139">IPersistStorage::Load</span><span class="sxs-lookup"><span data-stu-id="d8f92-139">IPersistStorage::Load</span></span>](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="d8f92-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="d8f92-140">IPersistStream::Load</span></span>](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="d8f92-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="d8f92-141">IPersistFile::Load</span></span>](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

