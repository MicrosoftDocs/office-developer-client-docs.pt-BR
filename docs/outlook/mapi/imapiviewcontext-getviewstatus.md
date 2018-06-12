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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: fb543f4188578483333614cb5768f903c9f243d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767393"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="6005f-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="6005f-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="6005f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6005f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6005f-105">Recupera o status atual do visualizador.</span><span class="sxs-lookup"><span data-stu-id="6005f-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="6005f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6005f-106">Parameters</span></span>

 <span data-ttu-id="6005f-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="6005f-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="6005f-108">[out] Ponteiro para uma bitmask dos sinalizadores fornecendo o status do visualizador.</span><span class="sxs-lookup"><span data-stu-id="6005f-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="6005f-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6005f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="6005f-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="6005f-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="6005f-111">Há uma mensagem anterior ou seguinte em outra categoria.</span><span class="sxs-lookup"><span data-stu-id="6005f-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="6005f-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="6005f-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="6005f-113">O formulário permite mensagens a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6005f-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="6005f-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="6005f-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="6005f-115">O formulário deve exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6005f-115">The form should display a user interface.</span></span> <span data-ttu-id="6005f-116">Se esse sinalizador não estiver definida, o formulário deve suprimir exibindo uma interface do usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="6005f-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="6005f-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="6005f-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="6005f-118">O formulário é modal do observador.</span><span class="sxs-lookup"><span data-stu-id="6005f-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="6005f-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="6005f-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="6005f-120">Há uma mensagem próxima no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="6005f-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="6005f-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="6005f-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="6005f-122">Há uma mensagem anterior no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="6005f-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="6005f-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="6005f-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="6005f-124">A mensagem deve ser aberta no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6005f-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="6005f-125">Excluir, enviar e mover as operações devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="6005f-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="6005f-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="6005f-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="6005f-127">Há uma mensagem não lida seguinte ou anterior no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="6005f-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6005f-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6005f-128">Return value</span></span>

<span data-ttu-id="6005f-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="6005f-129">S_OK</span></span> 
  
> <span data-ttu-id="6005f-130">Status do visualizador foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6005f-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6005f-131">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6005f-131">Remarks</span></span>

<span data-ttu-id="6005f-132">Objetos de formulário chamar o método **IMAPIViewContext::GetViewStatus** para determinar se há mais mensagens a ser ativada em um modo de formulário em um ou ambas as direções ou seja, na direção na qual um comando **seguida** ativa somente mensagens, além de direção na qual um comando **anterior** ativa mensagens, ou em ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="6005f-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="6005f-133">O valor apontado pelo parâmetro _lpulStatus_ é usado para determinar se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV são válidos para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="6005f-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="6005f-134">Se o sinalizador VCSTATUS_DELETE for definido, mas não o sinalizador VCSTATUS_READONLY, e em seguida, a mensagem pode ser excluída, usando o método [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="6005f-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="6005f-135">Normalmente, formulários desabilitar comandos de menu e botões se eles não são válidos para o contexto do visualizador.</span><span class="sxs-lookup"><span data-stu-id="6005f-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="6005f-136">Um visualizador alertando um formulário para uma alteração no status chamando o método [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="6005f-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="6005f-137">O sinalizador VCSTATUS_MODAL é definido se o formulário deve ser modal para a janela cujo identificador é passado na chamada [IMAPIForm::DoVerb](imapiform-doverb.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="6005f-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="6005f-138">Se VCSTATUS_MODAL for definido, o formulário pode usar o thread no qual a chamada **DoVerb** foi feita até que o formulário é fechado.</span><span class="sxs-lookup"><span data-stu-id="6005f-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="6005f-139">Se VCSTATUS_MODAL não estiver definida, o formulário não deve ser modal a esta janela e não deve usar o segmento.</span><span class="sxs-lookup"><span data-stu-id="6005f-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6005f-140">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6005f-140">MFCMAPI reference</span></span>

<span data-ttu-id="6005f-141">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6005f-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6005f-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6005f-142">**File**</span></span>|<span data-ttu-id="6005f-143">**Function**</span><span class="sxs-lookup"><span data-stu-id="6005f-143">**Function**</span></span>|<span data-ttu-id="6005f-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6005f-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6005f-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="6005f-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6005f-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="6005f-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="6005f-147">MFCMAPI implementa o método **IMAPIViewContext::GetViewStatus** nessa função.</span><span class="sxs-lookup"><span data-stu-id="6005f-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6005f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="6005f-148">See also</span></span>



[<span data-ttu-id="6005f-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="6005f-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="6005f-150">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6005f-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="6005f-151">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="6005f-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

