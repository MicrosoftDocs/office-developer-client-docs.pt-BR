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
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329453"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="7f521-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="7f521-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="7f521-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f521-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f521-105">Solicita que o formulário execute as tarefas associadas a um verbo específico.</span><span class="sxs-lookup"><span data-stu-id="7f521-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="7f521-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f521-106">Parameters</span></span>

 <span data-ttu-id="7f521-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="7f521-107">_iVerb_</span></span>
  
> <span data-ttu-id="7f521-108">[in] O número associado a um dos verbos do formulário.</span><span class="sxs-lookup"><span data-stu-id="7f521-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="7f521-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="7f521-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="7f521-110">[in] Um ponteiro para um objeto de contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="7f521-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="7f521-111">O _parâmetro lpViewContext_ pode ser **nulo.**</span><span class="sxs-lookup"><span data-stu-id="7f521-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="7f521-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="7f521-112">_hwndParent_</span></span>
  
> <span data-ttu-id="7f521-113">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="7f521-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="7f521-114">O  _parâmetro hwndParent_ deve ser **nulo se** a caixa de diálogo ou a janela não for modal.</span><span class="sxs-lookup"><span data-stu-id="7f521-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="7f521-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="7f521-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="7f521-116">[in] Um ponteiro para uma estrutura [de RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32 que contém o tamanho e a posição da janela do formulário.</span><span class="sxs-lookup"><span data-stu-id="7f521-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7f521-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7f521-117">Return value</span></span>

<span data-ttu-id="7f521-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f521-118">S_OK</span></span> 
  
> <span data-ttu-id="7f521-119">O verbo foi invocado com êxito.</span><span class="sxs-lookup"><span data-stu-id="7f521-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="7f521-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="7f521-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="7f521-121">O verbo representado pelo parâmetro  _iVerb_ é válido, mas o formulário não pode executar as operações atualmente associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="7f521-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7f521-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f521-122">Remarks</span></span>

<span data-ttu-id="7f521-123">Visualizadores de formulário chamam o método **IMAPIForm::D oVerb** para solicitar que o formulário execute as tarefas que ele associa a cada verbo que o formulário suporta.</span><span class="sxs-lookup"><span data-stu-id="7f521-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="7f521-124">Cada um dos verbos com suporte é identificado por um valor numérico, passado para **o DoVerb** no _parâmetro iVerb._</span><span class="sxs-lookup"><span data-stu-id="7f521-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="7f521-125">Implementações típicas **do DoVerb** contêm uma instrução **de** opção que testa os valores válidos para o  _parâmetro iVerb_ para o formulário.</span><span class="sxs-lookup"><span data-stu-id="7f521-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7f521-126">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7f521-126">Notes to implementers</span></span>

<span data-ttu-id="7f521-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span><span class="sxs-lookup"><span data-stu-id="7f521-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="7f521-128">Faça as alterações necessárias às suas estruturas de dados internas e não salve o contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="7f521-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="7f521-129">Execute as seguintes tarefas em sua **implementação do DoVerb:**</span><span class="sxs-lookup"><span data-stu-id="7f521-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="7f521-130">Execute qualquer código necessário para o verbo específico associado ao _parâmetro iVerb._</span><span class="sxs-lookup"><span data-stu-id="7f521-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="7f521-131">Se necessário, restaure o contexto do modo de exibição original.</span><span class="sxs-lookup"><span data-stu-id="7f521-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="7f521-132">Se um número de verbo desconhecido for passado, retorne MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="7f521-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="7f521-133">Caso contrário, retorne um resultado com base no sucesso ou falha de qualquer verbo que tenha sido executado.</span><span class="sxs-lookup"><span data-stu-id="7f521-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="7f521-134">Feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="7f521-134">Close the form.</span></span> <span data-ttu-id="7f521-135">É sempre sua responsabilidade fechar o formulário após a conclusão de uma chamada **do DoVerb.**</span><span class="sxs-lookup"><span data-stu-id="7f521-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="7f521-136">Alguns verbos, como Print, devem ser modais em relação à chamada **do DoVerb** — ou seja, a operação indicada deve ser concluída antes que a chamada **do DoVerb** seja retornada.</span><span class="sxs-lookup"><span data-stu-id="7f521-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="7f521-137">Para obter a **estrutura RECT** usada pela janela de um formulário, chame a [função GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="7f521-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="7f521-138">Não salve o alça no parâmetro  _hwndParent_ porque, embora ele normalmente permaneça válido até a conclusão do **DoVerb,** ele pode ser destruído imediatamente após o retorno da chamada.</span><span class="sxs-lookup"><span data-stu-id="7f521-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7f521-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7f521-139">Notes to callers</span></span>

<span data-ttu-id="7f521-140">Você pode fazer verbos não modais atuarem como verbos modais apontando _lpViewContext_ para uma implementação de contexto de exibição que retorna o sinalizador VCSTATUS_MODAL de seu método [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md)</span><span class="sxs-lookup"><span data-stu-id="7f521-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="7f521-141">Para obter mais informações sobre verbos em MAPI, consulte [Verbos de formulário.](form-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="7f521-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="7f521-142">Para obter mais informações sobre como os verbos são tratados no OLE, consulte [OLE e Transferência de Dados.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f521-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7f521-143">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7f521-143">MFCMAPI reference</span></span>

<span data-ttu-id="7f521-144">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f521-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7f521-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7f521-145">**File**</span></span>|<span data-ttu-id="7f521-146">**Função**</span><span class="sxs-lookup"><span data-stu-id="7f521-146">**Function**</span></span>|<span data-ttu-id="7f521-147">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="7f521-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f521-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7f521-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7f521-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="7f521-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="7f521-150">MFCMAPI usa o **método IMAPIForm::D oVerb** para invocar um verbo em um formulário.</span><span class="sxs-lookup"><span data-stu-id="7f521-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f521-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f521-151">See also</span></span>



[<span data-ttu-id="7f521-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="7f521-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="7f521-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="7f521-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="7f521-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f521-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="7f521-155">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7f521-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7f521-156">Verbos de formulário</span><span class="sxs-lookup"><span data-stu-id="7f521-156">Form Verbs</span></span>](form-verbs.md)

