---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe6270d82d227f52dfd5dfa5454c73e815ad9f42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573814"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="8307f-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="8307f-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="8307f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8307f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8307f-105">Solicita que o formulário execute qualquer item das tarefas ele associa um verbo específico.</span><span class="sxs-lookup"><span data-stu-id="8307f-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="8307f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8307f-106">Parameters</span></span>

 <span data-ttu-id="8307f-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="8307f-107">_iVerb_</span></span>
  
> <span data-ttu-id="8307f-108">[in] O número associado a um dos verbos do formulário.</span><span class="sxs-lookup"><span data-stu-id="8307f-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="8307f-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="8307f-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="8307f-110">[in] Um ponteiro para um objeto de contexto do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="8307f-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="8307f-111">O parâmetro _lpViewContext_ pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="8307f-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="8307f-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="8307f-112">_hwndParent_</span></span>
  
> <span data-ttu-id="8307f-113">[in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="8307f-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="8307f-114">O parâmetro _hwndParent_ deve ser **Nulo** se a caixa de diálogo ou a janela não é modal.</span><span class="sxs-lookup"><span data-stu-id="8307f-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="8307f-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="8307f-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="8307f-116">[in] Um ponteiro para um Win32 estrutura [Retangular](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário.</span><span class="sxs-lookup"><span data-stu-id="8307f-116">[in] A pointer to a Win32 [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8307f-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8307f-117">Return value</span></span>

<span data-ttu-id="8307f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8307f-118">S_OK</span></span> 
  
> <span data-ttu-id="8307f-119">O verbo com êxito foi invocado.</span><span class="sxs-lookup"><span data-stu-id="8307f-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="8307f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="8307f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="8307f-121">O verbo representado pelo parâmetro _iVerb_ é válido, mas o formulário não é possível executar as operações atualmente associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="8307f-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8307f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8307f-122">Remarks</span></span>

<span data-ttu-id="8307f-123">Visualizadores de formulário chame o método de **IMAPIForm::DoVerb** para solicitar que o formulário execute as tarefas que ela associa a cada verbo que o formulário oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="8307f-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="8307f-124">Cada um dos verbos com suporte é identificado por um valor numérico, passado para **DoVerb** no parâmetro _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="8307f-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="8307f-125">Implementações típicas dos **DoVerb** contenham uma instrução **switch** que testa os valores válidos para o parâmetro _iVerb_ para o formulário.</span><span class="sxs-lookup"><span data-stu-id="8307f-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8307f-126">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="8307f-126">Notes to implementers</span></span>

<span data-ttu-id="8307f-127">Se a tela de formulário especifica um contexto de modo de exibição no parâmetro _lpViewContext_ , usá-lo na sua implementação **DoVerb** em vez do contexto de modo de exibição passada em uma chamada anterior para o método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="8307f-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="8307f-128">Fazer as alterações necessárias para suas estruturas de dados interno e não salve o contexto de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="8307f-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="8307f-129">Execute as seguintes tarefas na sua implementação **DoVerb** :</span><span class="sxs-lookup"><span data-stu-id="8307f-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="8307f-130">Execute qualquer código é necessário para o verbo específico que está associado com o parâmetro _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="8307f-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="8307f-131">Se necessário, restaure o contexto de modo de exibição original.</span><span class="sxs-lookup"><span data-stu-id="8307f-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="8307f-132">Se um número de verbo desconhecido foi passado, retorne MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="8307f-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="8307f-133">Caso contrário, retornar um resultado baseado no sucesso ou falha de qualquer verbo foi executada.</span><span class="sxs-lookup"><span data-stu-id="8307f-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="8307f-134">Feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="8307f-134">Close the form.</span></span> <span data-ttu-id="8307f-135">É sempre fechar o formulário após a conclusão de uma chamada **DoVerb** sua responsabilidade.</span><span class="sxs-lookup"><span data-stu-id="8307f-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="8307f-136">Alguns verbos, como imprimir, devem ser modais com relação a chamada **DoVerb** — ou seja, a operação indicada deve ser concluída antes da chamada **DoVerb** retorna.</span><span class="sxs-lookup"><span data-stu-id="8307f-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="8307f-137">Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função de [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="8307f-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="8307f-138">Não salve a alça no parâmetro _hwndParent_ porque, embora ele geralmente permanecerá válido até a conclusão da **DoVerb**, ele pode ser destruído imediatamente após retornar da chamada.</span><span class="sxs-lookup"><span data-stu-id="8307f-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8307f-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8307f-139">Notes to callers</span></span>

<span data-ttu-id="8307f-140">Você pode fazer com que não restrita verbos agir como verbos modais, apontando _lpViewContext_ para uma implementação de contexto do modo de exibição que retorna o sinalizador VCSTATUS_MODAL de seu método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="8307f-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="8307f-141">Para obter mais informações sobre os verbos na MAPI, consulte [Verbos de formulário](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="8307f-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="8307f-142">Para obter mais informações sobre como os verbos são manipulados no OLE, consulte [OLE e transferência de dados](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8307f-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8307f-143">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8307f-143">MFCMAPI reference</span></span>

<span data-ttu-id="8307f-144">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8307f-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8307f-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="8307f-145">**File**</span></span>|<span data-ttu-id="8307f-146">**Function**</span><span class="sxs-lookup"><span data-stu-id="8307f-146">**Function**</span></span>|<span data-ttu-id="8307f-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8307f-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8307f-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="8307f-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="8307f-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="8307f-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="8307f-150">MFCMAPI usa o método **IMAPIForm::DoVerb** para invocar um verbo em um formulário.</span><span class="sxs-lookup"><span data-stu-id="8307f-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8307f-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="8307f-151">See also</span></span>



[<span data-ttu-id="8307f-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="8307f-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="8307f-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="8307f-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="8307f-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8307f-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="8307f-155">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="8307f-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8307f-156">Verbos de formulário</span><span class="sxs-lookup"><span data-stu-id="8307f-156">Form Verbs</span></span>](form-verbs.md)

