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
ms.openlocfilehash: 26ca126603ac1e695bd14a10cd8d9e637382b2e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584300"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="1892d-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="1892d-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="1892d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1892d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1892d-105">Estabelece um contexto de modo de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="1892d-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="1892d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1892d-106">Parameters</span></span>

 <span data-ttu-id="1892d-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="1892d-107">_pViewContext_</span></span>
  
> <span data-ttu-id="1892d-108">[in] Um ponteiro para o novo contexto de modo de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="1892d-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1892d-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1892d-109">Return value</span></span>

<span data-ttu-id="1892d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1892d-110">S_OK</span></span> 
  
> <span data-ttu-id="1892d-111">O contexto de modo de exibição foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="1892d-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1892d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1892d-112">Remarks</span></span>

<span data-ttu-id="1892d-113">Visualizadores de formulário chame o método de **IMAPIForm::SetViewContext** para estabelecer um contexto de modo de exibição de formulário específico como o atual.</span><span class="sxs-lookup"><span data-stu-id="1892d-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="1892d-114">Um formulário pode ter apenas um contexto de modo de exibição de cada vez.</span><span class="sxs-lookup"><span data-stu-id="1892d-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1892d-115">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="1892d-115">Notes to implementers</span></span>

<span data-ttu-id="1892d-116">A maioria dos servidores de formulário implementar **SetViewContext** usando o algoritmo a seguir:</span><span class="sxs-lookup"><span data-stu-id="1892d-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="1892d-117">Cancelar o registro do formulário chamando o método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) com **null** no parâmetro _pmnvs_ se já existir um contexto de modo de exibição para o formulário e depois ligue para [IUnknown:: Release do contexto modo de exibição](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) método a diminuir sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="1892d-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="1892d-118">Se o novo contexto de modo de exibição não for **nula**, a chamada **IMAPIViewContext::SetAdviseSink** usando o parâmetro _pViewContext_ para configurar uma nova exibição aconselhe coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="1892d-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="1892d-119">Se o novo contexto de modo de exibição não for **nula**, chame o método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar quais sinalizadores de status foram definidos.</span><span class="sxs-lookup"><span data-stu-id="1892d-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="1892d-120">Se o novo contexto de modo de exibição não for **nula**, armazená-lo e chamar o método [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para incrementar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="1892d-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="1892d-121">Atualize quaisquer elementos de interface do usuário que dependem do contexto do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="1892d-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="1892d-122">Dependendo os sinalizadores de status retornados de **IMAPIViewContext::GetViewStatus**, **SetViewContext** também pode realizar outras ações.</span><span class="sxs-lookup"><span data-stu-id="1892d-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="1892d-123">Por exemplo, se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV forem retornados, **SetViewContext** pode habilitar os botões **próximo** e **anterior** para o novo contexto de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="1892d-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1892d-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1892d-124">MFCMAPI reference</span></span>

<span data-ttu-id="1892d-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1892d-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1892d-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1892d-126">**File**</span></span>|<span data-ttu-id="1892d-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="1892d-127">**Function**</span></span>|<span data-ttu-id="1892d-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1892d-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1892d-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1892d-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1892d-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="1892d-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="1892d-131">MFCMAPI usa o método **IMAPIForm::SetViewContext** para definir o contexto de exibição do MFCMAPI no formulário antes que o formulário é exibido.</span><span class="sxs-lookup"><span data-stu-id="1892d-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1892d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1892d-132">See also</span></span>



[<span data-ttu-id="1892d-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="1892d-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="1892d-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1892d-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="1892d-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1892d-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="1892d-136">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1892d-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

