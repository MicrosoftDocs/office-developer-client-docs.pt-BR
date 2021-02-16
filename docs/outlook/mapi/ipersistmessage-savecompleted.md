---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317133"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="b38cb-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="b38cb-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="b38cb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b38cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b38cb-105">Notifica o formulário de que uma operação de salvar foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b38cb-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="b38cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b38cb-106">Parameters</span></span>

<span data-ttu-id="b38cb-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="b38cb-107">_pMessage_</span></span>
  
> <span data-ttu-id="b38cb-108">[in] Um ponteiro para a mensagem recém-salva.</span><span class="sxs-lookup"><span data-stu-id="b38cb-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b38cb-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b38cb-109">Return value</span></span>

<span data-ttu-id="b38cb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b38cb-110">S_OK</span></span> 
  
> <span data-ttu-id="b38cb-111">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b38cb-111">The notification was successful.</span></span>
    
<span data-ttu-id="b38cb-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b38cb-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="b38cb-113">O _parâmetro pMessage_ é NULL e o formulário está no estado [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave.](handsoffaftersave-state.md)</span><span class="sxs-lookup"><span data-stu-id="b38cb-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="b38cb-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="b38cb-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="b38cb-115">O formulário não está em um dos seguintes estados:</span><span class="sxs-lookup"><span data-stu-id="b38cb-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="b38cb-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="b38cb-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="b38cb-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="b38cb-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="b38cb-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="b38cb-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="b38cb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b38cb-119">Remarks</span></span>

<span data-ttu-id="b38cb-120">O **método IPersistMessage::SaveCompleted** é chamado por um visualizador de formulário para notificar o formulário de que todas as alterações pendentes foram salvas.</span><span class="sxs-lookup"><span data-stu-id="b38cb-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="b38cb-121">**SaveCompleted** deve ser chamado somente quando o formulário estiver em um dos seguintes estados:</span><span class="sxs-lookup"><span data-stu-id="b38cb-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="b38cb-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="b38cb-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="b38cb-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="b38cb-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="b38cb-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="b38cb-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b38cb-125">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b38cb-125">Notes to implementers</span></span>

<span data-ttu-id="b38cb-126">Há várias ações possíveis que o **método SaveCompleted** pode executar, dependendo do parâmetro do ponteiro da mensagem e do estado em que a mensagem está.</span><span class="sxs-lookup"><span data-stu-id="b38cb-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="b38cb-127">No entanto, quando uma ação for bem-sucedida, salve sempre o estado atual da mensagem que o parâmetro _pMessage_ aponta e transirá o formulário para seu [estado Normal.](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="b38cb-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="b38cb-128">A tabela a seguir descreve as condições que afetam as ações que você deve tomar na implementação **de SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="b38cb-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="b38cb-129">**Condition**</span><span class="sxs-lookup"><span data-stu-id="b38cb-129">**Condition**</span></span>|<span data-ttu-id="b38cb-130">**Ação**</span><span class="sxs-lookup"><span data-stu-id="b38cb-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b38cb-131">O  _parâmetro pMessage_ é NULL e  _o parâmetro fSameAsLoad_ do método [IPersistMessage::Save](ipersistmessage-save.md) é definido como TRUE.</span><span class="sxs-lookup"><span data-stu-id="b38cb-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="b38cb-132">Chame o [método IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b38cb-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b38cb-133">O  _parâmetro pMessage_ é NULL e  _o parâmetro fSameAsLoad_ do método **IPersistMessage::Save** é definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="b38cb-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="b38cb-134">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b38cb-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b38cb-135">O formulário está no estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="b38cb-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="b38cb-136">Libere a mensagem atual e substitua-a pela mensagem apontada pelo _parâmetro pMessage._</span><span class="sxs-lookup"><span data-stu-id="b38cb-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="b38cb-137">Chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da mensagem de substituição e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b38cb-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b38cb-138">O formulário está no estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="b38cb-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="b38cb-139">Chame o **método IMAPIViewAdviseSink::OnSaved** de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b38cb-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b38cb-140">O formulário está no [estado NoScribble.](noscribble-state.md)</span><span class="sxs-lookup"><span data-stu-id="b38cb-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="b38cb-141">Libere a mensagem atual e substitua-a pela mensagem apontada por  _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="b38cb-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="b38cb-142">Chame o método **IUnknown::AddRef** da mensagem de substituição.</span><span class="sxs-lookup"><span data-stu-id="b38cb-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="b38cb-143">Chame o **método IMAPIViewAdviseSink::OnSaved** de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b38cb-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b38cb-144">O formulário está em um dos estados HandsOff e o  _parâmetro pMessage_ está definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="b38cb-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="b38cb-145">Retornar E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="b38cb-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="b38cb-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span><span class="sxs-lookup"><span data-stu-id="b38cb-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="b38cb-147">Retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b38cb-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="b38cb-148">Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação dos métodos [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted)</span><span class="sxs-lookup"><span data-stu-id="b38cb-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b38cb-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b38cb-149">See also</span></span>

- [<span data-ttu-id="b38cb-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b38cb-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="b38cb-151">Estados do formulário</span><span class="sxs-lookup"><span data-stu-id="b38cb-151">Form States</span></span>](form-states.md)
