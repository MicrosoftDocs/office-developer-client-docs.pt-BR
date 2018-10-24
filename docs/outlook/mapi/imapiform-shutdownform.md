---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384833"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="00ffd-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="00ffd-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="00ffd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ffd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ffd-105">Fecha o formulário.</span><span class="sxs-lookup"><span data-stu-id="00ffd-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="00ffd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00ffd-106">Parameters</span></span>

 <span data-ttu-id="00ffd-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="00ffd-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="00ffd-108">[in] Um valor que controla como ou se os dados do formulário são salvos antes que o formulário é fechado.</span><span class="sxs-lookup"><span data-stu-id="00ffd-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="00ffd-109">Um dos sinalizadores a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="00ffd-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="00ffd-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="00ffd-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="00ffd-111">Dados do formulário não devem ser salvo.</span><span class="sxs-lookup"><span data-stu-id="00ffd-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="00ffd-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="00ffd-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="00ffd-113">O usuário deve ser solicitado a salvar os dados alterados no formulário.</span><span class="sxs-lookup"><span data-stu-id="00ffd-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="00ffd-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="00ffd-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="00ffd-115">Dados do formulário devem ser salvo se tiver sido alterado desde a última salvar.</span><span class="sxs-lookup"><span data-stu-id="00ffd-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="00ffd-116">Se nenhuma interface de usuário que está sendo exibido, o formulário opcionalmente pode alternar para usar a funcionalidade para a opção SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="00ffd-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00ffd-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="00ffd-117">Return value</span></span>

<span data-ttu-id="00ffd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="00ffd-118">S_OK</span></span> 
  
> <span data-ttu-id="00ffd-119">O formulário foi fechado.</span><span class="sxs-lookup"><span data-stu-id="00ffd-119">The form was closed.</span></span>
    
<span data-ttu-id="00ffd-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="00ffd-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="00ffd-121">O formulário já foi fechado por uma chamada anterior ao **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="00ffd-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00ffd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="00ffd-122">Remarks</span></span>

<span data-ttu-id="00ffd-123">Visualizadores de formulário chame o método **IMAPIForm::ShutdownForm** para fechar um formulário.</span><span class="sxs-lookup"><span data-stu-id="00ffd-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="00ffd-124">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="00ffd-124">Notes to implementers</span></span>

<span data-ttu-id="00ffd-125">Execute as seguintes tarefas na sua implementação de **ShutdownForm**:</span><span class="sxs-lookup"><span data-stu-id="00ffd-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="00ffd-126">Verifique se um visualizador já não chamado **ShutdownForm**e retornar E_UNEXPECTED se ele tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="00ffd-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="00ffd-127">Embora esta seja improvável, você deve verificar.</span><span class="sxs-lookup"><span data-stu-id="00ffd-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="00ffd-128">Chame o método de [AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do seu formulário para que o armazenamento para o formulário e qualquer estruturas de dados internos permaneça disponível até que o processamento está concluído.</span><span class="sxs-lookup"><span data-stu-id="00ffd-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="00ffd-129">Determine se há quaisquer alterações não salvas os dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="00ffd-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="00ffd-130">Salve os dados de acordo com como o parâmetro _ulSaveOptions_ é definido chamando o método de [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) do seu visualizador.</span><span class="sxs-lookup"><span data-stu-id="00ffd-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="00ffd-131">Destrua a janela de interface de usuário do seu formulário.</span><span class="sxs-lookup"><span data-stu-id="00ffd-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="00ffd-132">Libere mensagem e os objetos de site de seu formulário chamando os métodos [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00ffd-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="00ffd-133">Notifica registrados todos os visualizadores do desligamento pendente chamando os métodos [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="00ffd-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="00ffd-134">Chame o método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar o registro do formulário para fins de notificação, definindo o ponteiro de coletor de eventos advise como **Nulo**.</span><span class="sxs-lookup"><span data-stu-id="00ffd-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="00ffd-135">Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para as propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="00ffd-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="00ffd-136">Chame o método de **IUnknown:: Release** do seu formulário, correspondentes a chamada **AddRef** feita na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="00ffd-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="00ffd-137">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="00ffd-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="00ffd-138">Depois que essas ações tenham sido concluídas, os métodos só é válidos no objeto de formulário que podem ser chamadas são aqueles da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00ffd-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00ffd-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="00ffd-139">Notes to callers</span></span>

<span data-ttu-id="00ffd-140">Quando **ShutdownForm** retorna, independentemente se ele retornará um erro, libere o formulário chamando seu método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="00ffd-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="00ffd-141">Você pode ignorar com segurança os erros retornados pelo **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="00ffd-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00ffd-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="00ffd-142">See also</span></span>



[<span data-ttu-id="00ffd-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="00ffd-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="00ffd-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="00ffd-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="00ffd-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="00ffd-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="00ffd-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00ffd-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00ffd-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00ffd-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

