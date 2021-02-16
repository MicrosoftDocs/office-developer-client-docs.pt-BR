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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329474"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="7b056-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="7b056-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="7b056-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b056-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b056-105">Fecha o formulário.</span><span class="sxs-lookup"><span data-stu-id="7b056-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="7b056-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b056-106">Parameters</span></span>

 <span data-ttu-id="7b056-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="7b056-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="7b056-108">[in] Um valor que controla como ou se os dados no formulário são salvos antes de o formulário ser fechado.</span><span class="sxs-lookup"><span data-stu-id="7b056-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="7b056-109">Um dos sinalizadores a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7b056-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="7b056-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="7b056-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="7b056-111">Os dados do formulário não devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="7b056-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="7b056-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="7b056-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="7b056-113">O usuário deve ser solicitado a salvar quaisquer dados alterados no formulário.</span><span class="sxs-lookup"><span data-stu-id="7b056-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="7b056-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="7b056-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="7b056-115">Os dados do formulário devem ser salvos se eles foram alterados desde o último salvar.</span><span class="sxs-lookup"><span data-stu-id="7b056-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="7b056-116">Se nenhuma interface do usuário estiver sendo exibida, o formulário pode, opcionalmente, alternar para usar a funcionalidade para a SAVEOPTS_NOSAVE opção.</span><span class="sxs-lookup"><span data-stu-id="7b056-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b056-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7b056-117">Return value</span></span>

<span data-ttu-id="7b056-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b056-118">S_OK</span></span> 
  
> <span data-ttu-id="7b056-119">O formulário foi fechado.</span><span class="sxs-lookup"><span data-stu-id="7b056-119">The form was closed.</span></span>
    
<span data-ttu-id="7b056-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="7b056-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="7b056-121">O formulário já foi fechado por uma chamada anterior para **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="7b056-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b056-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b056-122">Remarks</span></span>

<span data-ttu-id="7b056-123">Visualizadores de formulário chamam **o método IMAPIForm::ShutdownForm** para fechar um formulário.</span><span class="sxs-lookup"><span data-stu-id="7b056-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b056-124">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7b056-124">Notes to implementers</span></span>

<span data-ttu-id="7b056-125">Execute as seguintes tarefas na implementação do **ShutdownForm:**</span><span class="sxs-lookup"><span data-stu-id="7b056-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="7b056-126">Verifique se um visualizador ainda não chamou **ShutdownForm** e retorne E_UNEXPECTED se tiver sido.</span><span class="sxs-lookup"><span data-stu-id="7b056-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="7b056-127">Embora isso seja improvável, você deve verificar.</span><span class="sxs-lookup"><span data-stu-id="7b056-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="7b056-128">Chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do formulário para que o armazenamento do formulário e de todas as estruturas de dados internas permaneçam disponíveis até que o processamento seja concluído.</span><span class="sxs-lookup"><span data-stu-id="7b056-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="7b056-129">Determine se há alguma alteração não sedada nos dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="7b056-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="7b056-130">Salve dados não salvo de acordo com o modo como o  _parâmetro ulSaveOptions_ é definido chamando o método [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) do visualizador.</span><span class="sxs-lookup"><span data-stu-id="7b056-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="7b056-131">Destruir a janela da interface do usuário do formulário.</span><span class="sxs-lookup"><span data-stu-id="7b056-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="7b056-132">Libere os objetos de site de mensagem e mensagem do formulário chamando seus métodos [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b056-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="7b056-133">Notifique todos os visualizadores registrados sobre o desligamento pendente chamando seus métodos [IMAPIViewAdviseSink::OnShutdown.](imapiviewadvisesink-onshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="7b056-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="7b056-134">Chame o [método IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar o registro do seu formulário para notificação definindo o ponteiro do pia de aviso como **nulo.**</span><span class="sxs-lookup"><span data-stu-id="7b056-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="7b056-135">Chame a [função MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para as propriedades do seu formulário.</span><span class="sxs-lookup"><span data-stu-id="7b056-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="7b056-136">Chame o método **IUnknown::Release** do formulário, correspondendo à chamada **AddRef** feita na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="7b056-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="7b056-137">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="7b056-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7b056-138">Depois que essas ações foram concluídas, os únicos métodos válidos no objeto de formulário que podem ser chamados são aqueles da interface [IUnknown.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b056-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b056-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7b056-139">Notes to callers</span></span>

<span data-ttu-id="7b056-140">Quando **ShutdownForm** retornar, independentemente de retornar um erro, libere o formulário chamando seu **método IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="7b056-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="7b056-141">Você pode ignorar com segurança quaisquer erros retornados pelo **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="7b056-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b056-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b056-142">See also</span></span>



[<span data-ttu-id="7b056-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="7b056-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="7b056-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="7b056-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="7b056-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7b056-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="7b056-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7b056-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7b056-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b056-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

