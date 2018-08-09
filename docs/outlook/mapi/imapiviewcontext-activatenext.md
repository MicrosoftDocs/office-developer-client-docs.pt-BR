---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 150a0c6eb7efa83f5ff1d12d915351bf5ca9d45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767380"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="44143-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="44143-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="44143-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44143-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44143-105">Ativa a mensagem anterior ou seguinte na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="44143-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="44143-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44143-106">Parameters</span></span>

<span data-ttu-id="44143-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="44143-107">_ulDir_</span></span>
  
> <span data-ttu-id="44143-108">[in] Sinalizadores de status oferecendo informações sobre a mensagem a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="44143-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="44143-109">Configurações de sinalizador válidos são:</span><span class="sxs-lookup"><span data-stu-id="44143-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="44143-110">VCDIR_CATEGORY: O Visualizador deve ativar uma mensagem em outra categoria do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="44143-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="44143-111">A mensagem a ser ativada é:</span><span class="sxs-lookup"><span data-stu-id="44143-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="44143-112">A primeira mensagem na categoria próxima modo de exibição se esse sinalizador for ed **ou**com VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="44143-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="44143-113">A última mensagem da categoria do modo de exibição anterior se esse sinalizador for **OR**ed com VCDIR_PREV e a categoria anterior é expandida.</span><span class="sxs-lookup"><span data-stu-id="44143-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="44143-114">A primeira mensagem na categoria exibir anterior se esse sinalizador for **OR**ed com VCDIR_PREV e a categoria anterior não será expandida.</span><span class="sxs-lookup"><span data-stu-id="44143-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="44143-115">Nesse caso, a categoria anterior passa por expansão automática.</span><span class="sxs-lookup"><span data-stu-id="44143-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="44143-116">VCDIR_DELETE: O Visualizador deve ativar a mensagem anterior ou seguinte porque a mensagem atual foi excluída.</span><span class="sxs-lookup"><span data-stu-id="44143-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="44143-117">VCDIR_MOVE: O Visualizador deve ativar a mensagem anterior ou seguinte porque a mensagem atual foi movida.</span><span class="sxs-lookup"><span data-stu-id="44143-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="44143-118">VCDIR_NEXT: O Visualizador deve ativar a próxima mensagem na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="44143-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="44143-119">VCDIR_PREV: O Visualizador deve ativar a mensagem anterior na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="44143-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="44143-120">VCDIR_UNREAD: O Visualizador deve ativar a mensagem não lida seguinte ou anterior na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="44143-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="44143-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="44143-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="44143-122">[in] Ponteiro para um Windows **Retangular** estruturar contendo o tamanho e a posição da janela a ser usado para exibir a mensagem ativada.</span><span class="sxs-lookup"><span data-stu-id="44143-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44143-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="44143-123">Return value</span></span>

<span data-ttu-id="44143-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="44143-124">S_OK</span></span> 
  
> <span data-ttu-id="44143-125">A mensagem foi ativada com êxito.</span><span class="sxs-lookup"><span data-stu-id="44143-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="44143-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="44143-126">S_FALSE</span></span> 
  
> <span data-ttu-id="44143-127">A mensagem foi ativada com êxito, mas um tipo diferente de formulário foi aberto no processo.</span><span class="sxs-lookup"><span data-stu-id="44143-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44143-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="44143-128">Remarks</span></span>

<span data-ttu-id="44143-129">Objetos de formulário chame o método de **IMAPIViewContext::ActivateNext** para alterar o que mensagem é exibida ao usuário.</span><span class="sxs-lookup"><span data-stu-id="44143-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="44143-130">O valor passado no parâmetro _ulDir_ indica qual mensagem deve ser ativado e, em alguns casos, o motivo.</span><span class="sxs-lookup"><span data-stu-id="44143-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="44143-131">Os sinalizadores VCDIR_NEXT e VCDIR_PREVIOUS correspondem aos usuários, escolha o comando **próximo** ou **anterior** em um modo de exibição, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="44143-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="44143-132">Essas operações geralmente correspondem ao mover para cima ou para baixo uma mensagem na lista do Visualizador de formulário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="44143-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="44143-133">Os sinalizadores VCDIR_DELETE e VCDIR_MOVE são definidos por [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) e [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) métodos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="44143-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="44143-134">Implementações desses métodos chamar **ActivateNext** com direção apropriada e, em seguida, executam a operação solicitada na mensagem se a chamada **ActivateNext** não falhou.</span><span class="sxs-lookup"><span data-stu-id="44143-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="44143-135">Visualizadores de formulário normalmente habilitar usuários especificar a direção para mover-se na lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="44143-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="44143-136">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="44143-136">Notes to implementers</span></span>

<span data-ttu-id="44143-137">A implementação dos [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) torna a mensagem anterior ou seguinte na pasta, dependendo do valor da _ulDir_, a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="44143-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="44143-138">Após **ActivateNext** retorna, chame [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obter um ponteiro para a mensagem recentemente ativada.</span><span class="sxs-lookup"><span data-stu-id="44143-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="44143-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="44143-139">Notes to callers</span></span>

<span data-ttu-id="44143-140">Se **ActivateNext** retorna S_FALSE, ou se uma mensagem atual não estiver presente, execute o procedimento de desligamento normal que deve incluir a chamar o método de [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) do seu formulário.</span><span class="sxs-lookup"><span data-stu-id="44143-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="44143-141">Se for exibida uma mensagem seguinte ou anterior, use o retângulo de janela passado no parâmetro _prcPosRect_ para exibi-la.</span><span class="sxs-lookup"><span data-stu-id="44143-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="44143-142">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="44143-142">MFCMAPI reference</span></span>

<span data-ttu-id="44143-143">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="44143-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="44143-144">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="44143-144">**File**</span></span>|<span data-ttu-id="44143-145">**Function**</span><span class="sxs-lookup"><span data-stu-id="44143-145">**Function**</span></span>|<span data-ttu-id="44143-146">**Comment**</span><span class="sxs-lookup"><span data-stu-id="44143-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="44143-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="44143-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="44143-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="44143-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="44143-149">MFCMAPI implementa o método **IMAPIViewContext::ActivateNext** nessa função.</span><span class="sxs-lookup"><span data-stu-id="44143-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44143-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="44143-150">See also</span></span>

- [<span data-ttu-id="44143-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="44143-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="44143-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44143-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="44143-153">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="44143-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

