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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317126"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="4c2c2-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="4c2c2-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="4c2c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c2c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c2c2-105">Carrega o formulário para uma mensagem especificada.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4c2c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c2c2-106">Parameters</span></span>

 <span data-ttu-id="4c2c2-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="4c2c2-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="4c2c2-108">no Um ponteiro para o site da mensagem para o formulário a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="4c2c2-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="4c2c2-109">_pMessage_</span></span>
  
> <span data-ttu-id="4c2c2-110">no Um ponteiro para a mensagem para a qual o formulário deve ser carregado.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="4c2c2-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="4c2c2-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4c2c2-112">no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor, copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem, que fornecem informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="4c2c2-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="4c2c2-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4c2c2-114">no Uma bitmask de sinalizadores, copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem, que fornecem mais informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c2c2-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4c2c2-115">Return value</span></span>

<span data-ttu-id="4c2c2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c2c2-116">S_OK</span></span> 
  
> <span data-ttu-id="4c2c2-117">O formulário foi carregado com êxito.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c2c2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c2c2-118">Remarks</span></span>

<span data-ttu-id="4c2c2-119">Os visualizadores de formulários chamam o método **IPersistMessage:: Load** para carregar um formulário para uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4c2c2-120">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="4c2c2-120">Notes to implementers</span></span>

 <span data-ttu-id="4c2c2-121">**Load** é chamado somente quando um formulário está em um dos seguintes Estados:</span><span class="sxs-lookup"><span data-stu-id="4c2c2-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="4c2c2-122">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="4c2c2-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="4c2c2-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="4c2c2-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="4c2c2-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="4c2c2-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="4c2c2-125">Se um visualizador de formulários chamar **Load** enquanto o formulário estiver em qualquer outro Estado, o método retornará E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="4c2c2-126">Se o formulário tiver uma referência a um site de mensagem ativo diferente daquele que é passado para **carregar**, libere o site original porque ele não será mais usado.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="4c2c2-127">Armazene os ponteiros no site da mensagem e a mensagem dos parâmetros _pMessageSite_ e _PMessage_ e chame os métodos [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos dois objetos para incrementar suas contagens de referência.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="4c2c2-128">Após a conclusão de **AddRef** , armazene as propriedades dos parâmetros _ulMessageStatus_ e _ulMessageFlags_ no formulário.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="4c2c2-129">Migre o formulário para seu estado [normal](normal-state.md) antes de exibi-lo e notifique os visualizadores registrados chamando seus métodos [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2c2-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="4c2c2-130">Se nenhum erro ocorrer, retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="4c2c2-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c2c2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c2c2-131">See also</span></span>



[<span data-ttu-id="4c2c2-132">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="4c2c2-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="4c2c2-133">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="4c2c2-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="4c2c2-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c2c2-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="4c2c2-135">Estado não inicializado</span><span class="sxs-lookup"><span data-stu-id="4c2c2-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="4c2c2-136">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="4c2c2-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="4c2c2-137">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="4c2c2-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="4c2c2-138">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="4c2c2-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="4c2c2-139">IPersistStorage:: Load</span><span class="sxs-lookup"><span data-stu-id="4c2c2-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="4c2c2-140">IPersistStream:: Load</span><span class="sxs-lookup"><span data-stu-id="4c2c2-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="4c2c2-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="4c2c2-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

