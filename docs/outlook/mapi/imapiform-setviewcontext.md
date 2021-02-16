---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350943"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="7440b-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="7440b-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="7440b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7440b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7440b-105">Estabelece um contexto de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="7440b-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="7440b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7440b-106">Parameters</span></span>

 <span data-ttu-id="7440b-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="7440b-107">_pViewContext_</span></span>
  
> <span data-ttu-id="7440b-108">[in] Um ponteiro para o novo contexto de exibição do formulário.</span><span class="sxs-lookup"><span data-stu-id="7440b-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7440b-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7440b-109">Return value</span></span>

<span data-ttu-id="7440b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7440b-110">S_OK</span></span> 
  
> <span data-ttu-id="7440b-111">O contexto de exibição foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="7440b-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7440b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7440b-112">Remarks</span></span>

<span data-ttu-id="7440b-113">Visualizadores de formulário chamam o **método IMAPIForm::SetViewContext** para estabelecer um contexto de modo de exibição de formulário específico como atual.</span><span class="sxs-lookup"><span data-stu-id="7440b-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="7440b-114">Um formulário pode ter apenas um contexto de exibição por vez.</span><span class="sxs-lookup"><span data-stu-id="7440b-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7440b-115">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7440b-115">Notes to implementers</span></span>

<span data-ttu-id="7440b-116">A maioria dos servidores de formulário **implementam SetViewContext** usando o seguinte algoritmo:</span><span class="sxs-lookup"><span data-stu-id="7440b-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="7440b-117">Se já existir um contexto de exibição para o formulário, cancele o registro do formulário chamando  o método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) com nulo no parâmetro _pmnvs_ e, em seguida, chame o método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do contexto de exibição para diminui-la.</span><span class="sxs-lookup"><span data-stu-id="7440b-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="7440b-118">Se o novo contexto de exibição não for nulo, chame **IMAPIViewContext::SetAdviseSink** usando o parâmetro _pViewContext_ para configurar um novo sink de alerta de exibição.</span><span class="sxs-lookup"><span data-stu-id="7440b-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="7440b-119">Se o novo contexto de modo de exibição não for nulo, chame o método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar quais sinalizadores de status foram definidos.</span><span class="sxs-lookup"><span data-stu-id="7440b-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="7440b-120">Se o novo contexto de modo de exibição não for nulo, armazene-o e chame seu método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para incrementar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="7440b-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="7440b-121">Atualize todos os elementos da interface do usuário que dependam do contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="7440b-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="7440b-122">Dependendo dos sinalizadores de status retornados de **IMAPIViewContext::GetViewStatus**, **SetViewContext** também pode executar outras ações.</span><span class="sxs-lookup"><span data-stu-id="7440b-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="7440b-123">Por exemplo, se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV são retornados, **SetViewContext** pode habilitar os botões Próximo e Anterior para o novo contexto de modo de exibição.  </span><span class="sxs-lookup"><span data-stu-id="7440b-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7440b-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7440b-124">MFCMAPI reference</span></span>

<span data-ttu-id="7440b-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7440b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7440b-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7440b-126">**File**</span></span>|<span data-ttu-id="7440b-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="7440b-127">**Function**</span></span>|<span data-ttu-id="7440b-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="7440b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7440b-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7440b-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7440b-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="7440b-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="7440b-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span><span class="sxs-lookup"><span data-stu-id="7440b-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7440b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7440b-132">See also</span></span>



[<span data-ttu-id="7440b-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="7440b-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="7440b-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7440b-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="7440b-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7440b-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="7440b-136">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7440b-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

