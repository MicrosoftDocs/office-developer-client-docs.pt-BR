---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429010"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="cb949-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="cb949-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="cb949-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb949-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb949-105">Recupera o status atual do visualizador.</span><span class="sxs-lookup"><span data-stu-id="cb949-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="cb949-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb949-106">Parameters</span></span>

 <span data-ttu-id="cb949-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="cb949-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="cb949-108">[out] Ponteiro para uma máscara de bits de sinalizadores que fornece o status do visualizador.</span><span class="sxs-lookup"><span data-stu-id="cb949-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="cb949-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="cb949-109">The following flags can be set:</span></span>
    
<span data-ttu-id="cb949-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="cb949-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="cb949-111">Há uma mensagem seguinte ou anterior em outra categoria.</span><span class="sxs-lookup"><span data-stu-id="cb949-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="cb949-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="cb949-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="cb949-113">O formulário permite que as mensagens sejam removidas.</span><span class="sxs-lookup"><span data-stu-id="cb949-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="cb949-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="cb949-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="cb949-115">O formulário deve exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="cb949-115">The form should display a user interface.</span></span> <span data-ttu-id="cb949-116">Se esse sinalizador não estiver definido, o formulário deverá suprimir a exibição de uma interface do usuário mesmo em resposta a um verbo que normalmente faz com que uma interface do usuário seja exibida.</span><span class="sxs-lookup"><span data-stu-id="cb949-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="cb949-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="cb949-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="cb949-118">O formulário é modal para o visualizador.</span><span class="sxs-lookup"><span data-stu-id="cb949-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="cb949-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="cb949-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="cb949-120">Há uma próxima mensagem no ponto de vista.</span><span class="sxs-lookup"><span data-stu-id="cb949-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="cb949-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="cb949-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="cb949-122">Há uma mensagem anterior na exibição.</span><span class="sxs-lookup"><span data-stu-id="cb949-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="cb949-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="cb949-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="cb949-124">A mensagem deve ser aberta no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cb949-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="cb949-125">As operações excluir, enviar e mover devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="cb949-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="cb949-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="cb949-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="cb949-127">Há uma próxima mensagem não lida ou anterior no visualização.</span><span class="sxs-lookup"><span data-stu-id="cb949-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb949-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cb949-128">Return value</span></span>

<span data-ttu-id="cb949-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb949-129">S_OK</span></span> 
  
> <span data-ttu-id="cb949-130">O status do visualizador foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="cb949-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb949-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb949-131">Remarks</span></span>

<span data-ttu-id="cb949-132">Objetos de formulário chamam o método **IMAPIViewContext::GetViewStatus** para determinar se há mais mensagens a serem ativadas em um modo de formulário em uma  ou ambas as direções, ou seja, na direção na qual um comando **Next** ativa mensagens, na direção em que um comando Previous ativa mensagens ou em ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="cb949-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="cb949-133">O valor apontado pelo parâmetro  _lpulStatus_ é usado para determinar se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV são válidos para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="cb949-134">Se o sinalizador VCSTATUS_DELETE estiver definido, mas não o sinalizador VCSTATUS_READONLY, a mensagem poderá ser excluída usando o método [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md)</span><span class="sxs-lookup"><span data-stu-id="cb949-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="cb949-135">Normalmente, os formulários desabilitam comandos e botões de menu se não são válidos para o contexto do visualizador.</span><span class="sxs-lookup"><span data-stu-id="cb949-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="cb949-136">Um visualizador pode alertar um formulário para uma alteração no status chamando seu [método IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md)</span><span class="sxs-lookup"><span data-stu-id="cb949-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="cb949-137">O VCSTATUS_MODAL é definido se o formulário deve ser modal para a janela cujo alça é passada na chamada [IMAPIForm::D oVerb](imapiform-doverb.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="cb949-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="cb949-138">Se VCSTATUS_MODAL for definida, o formulário poderá usar o thread no qual a chamada **do DoVerb** foi feita até que o formulário seja fechado.</span><span class="sxs-lookup"><span data-stu-id="cb949-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="cb949-139">Se VCSTATUS_MODAL não estiver definido, o formulário não deve ser modal para essa janela e não deve usar o thread.</span><span class="sxs-lookup"><span data-stu-id="cb949-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb949-140">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cb949-140">MFCMAPI reference</span></span>

<span data-ttu-id="cb949-141">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cb949-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb949-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="cb949-142">**File**</span></span>|<span data-ttu-id="cb949-143">**Função**</span><span class="sxs-lookup"><span data-stu-id="cb949-143">**Function**</span></span>|<span data-ttu-id="cb949-144">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="cb949-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb949-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="cb949-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="cb949-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="cb949-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="cb949-147">MFCMAPI implementa o **método IMAPIViewContext::GetViewStatus** nesta função.</span><span class="sxs-lookup"><span data-stu-id="cb949-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb949-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb949-148">See also</span></span>



[<span data-ttu-id="cb949-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="cb949-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="cb949-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb949-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="cb949-151">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="cb949-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

