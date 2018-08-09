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
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767617"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="db0f2-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="db0f2-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="db0f2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db0f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db0f2-105">Notifica o formulário que uma gravação operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="db0f2-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="db0f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db0f2-106">Parameters</span></span>

<span data-ttu-id="db0f2-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="db0f2-107">_pMessage_</span></span>
  
> <span data-ttu-id="db0f2-108">[in] Um ponteiro para a mensagem salva recentemente.</span><span class="sxs-lookup"><span data-stu-id="db0f2-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db0f2-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="db0f2-109">Return value</span></span>

<span data-ttu-id="db0f2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="db0f2-110">S_OK</span></span> 
  
> <span data-ttu-id="db0f2-111">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db0f2-111">The notification was successful.</span></span>
    
<span data-ttu-id="db0f2-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="db0f2-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="db0f2-113">O parâmetro _pMessage_ é NULL e o formulário está no estado de [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="db0f2-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="db0f2-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="db0f2-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="db0f2-115">O formulário não estiver em um dos seguintes estados:</span><span class="sxs-lookup"><span data-stu-id="db0f2-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="db0f2-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="db0f2-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="db0f2-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="db0f2-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="db0f2-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="db0f2-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="db0f2-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="db0f2-119">Remarks</span></span>

<span data-ttu-id="db0f2-120">O método **IPersistMessage::SaveCompleted** é chamado por um visualizador de formulário para notificar o formulário que foram salvos todas as alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="db0f2-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="db0f2-121">**SaveCompleted** deve ser chamado apenas quando o formulário está em um dos seguintes estados:</span><span class="sxs-lookup"><span data-stu-id="db0f2-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="db0f2-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="db0f2-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="db0f2-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="db0f2-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="db0f2-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="db0f2-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="db0f2-125">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="db0f2-125">Notes to implementers</span></span>

<span data-ttu-id="db0f2-126">Existem várias ações possíveis que o método **SaveCompleted** pode realizar, dependendo do que a mensagem contém o parâmetro de ponteiro e estado da qual a mensagem está em.</span><span class="sxs-lookup"><span data-stu-id="db0f2-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="db0f2-127">No entanto, quando uma ação for bem-sucedido, sempre salve o estado atual da mensagem que o parâmetro _pMessage_ aponta para e transição o formulário ao seu estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="db0f2-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="db0f2-128">A tabela a seguir descreve as condições que afetam as ações que você deve tomar na sua implementação de **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="db0f2-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="db0f2-129">**Condição**</span><span class="sxs-lookup"><span data-stu-id="db0f2-129">**Condition**</span></span>|<span data-ttu-id="db0f2-130">**Action**</span><span class="sxs-lookup"><span data-stu-id="db0f2-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db0f2-131">O parâmetro _pMessage_ é NULL e o parâmetro _fSameAsLoad_ do método [IPersistMessage::Save](ipersistmessage-save.md) é definido como TRUE.</span><span class="sxs-lookup"><span data-stu-id="db0f2-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="db0f2-132">Chame o método [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) todos os visualizadores registrados, marcar o formulário como S_OK limpa e retorno.</span><span class="sxs-lookup"><span data-stu-id="db0f2-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="db0f2-133">O parâmetro _pMessage_ é NULL e o parâmetro _fSameAsLoad_ do método **IPersistMessage::Save** é definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="db0f2-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="db0f2-134">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="db0f2-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="db0f2-135">O formulário está no estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="db0f2-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="db0f2-136">Liberar a mensagem atual e substituí-la com a mensagem apontada pelo parâmetro _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="db0f2-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="db0f2-137">Método de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da mensagem substituição de chamada e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="db0f2-137">Call the replacement message's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="db0f2-138">O formulário está no estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="db0f2-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="db0f2-139">Chame o método **IMAPIViewAdviseSink::OnSaved** todos os visualizadores registrados, marcar o formulário como S_OK limpa e retorno.</span><span class="sxs-lookup"><span data-stu-id="db0f2-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="db0f2-140">O formulário está no estado [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="db0f2-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="db0f2-141">Liberar a mensagem atual e substituí-la com a mensagem apontada pela _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="db0f2-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="db0f2-142">Chame o método de **AddRef** da mensagem de substituição.</span><span class="sxs-lookup"><span data-stu-id="db0f2-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="db0f2-143">Chame o método **IMAPIViewAdviseSink::OnSaved** todos os visualizadores registrados, marcar o formulário como S_OK limpa e retorno.</span><span class="sxs-lookup"><span data-stu-id="db0f2-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="db0f2-144">O formulário está em um dos Estados HandsOff e o parâmetro _pMessage_ é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="db0f2-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="db0f2-145">Retorne E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="db0f2-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="db0f2-146">O formulário está em um estado que não seja um dos Estados HandsOff ou o estado de NoScribble.</span><span class="sxs-lookup"><span data-stu-id="db0f2-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="db0f2-147">Retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="db0f2-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="db0f2-148">Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação para os métodos [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) ou [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="db0f2-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) or [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db0f2-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="db0f2-149">See also</span></span>



[<span data-ttu-id="db0f2-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db0f2-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="db0f2-151">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="db0f2-151">Form States</span></span>](form-states.md)


[<span data-ttu-id="db0f2-152">IPersistStorage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="db0f2-152">IPersistStorage::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[<span data-ttu-id="db0f2-153">IPersistFile::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="db0f2-153">IPersistFile::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)

