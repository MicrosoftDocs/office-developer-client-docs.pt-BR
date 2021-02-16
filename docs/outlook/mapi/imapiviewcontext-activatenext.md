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
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410613"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="b8431-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="b8431-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="b8431-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8431-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8431-105">Ativa a mensagem seguinte ou anterior na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8431-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="b8431-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8431-106">Parameters</span></span>

<span data-ttu-id="b8431-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="b8431-107">_ulDir_</span></span>
  
> <span data-ttu-id="b8431-108">[in] Sinalizadores de status que dão informações sobre a mensagem a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="b8431-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="b8431-109">As configurações de sinalizador válidas são:</span><span class="sxs-lookup"><span data-stu-id="b8431-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="b8431-110">VCDIR_CATEGORY: o visualizador deve ativar uma mensagem em outra categoria do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8431-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="b8431-111">A mensagem a ser ativada é:</span><span class="sxs-lookup"><span data-stu-id="b8431-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="b8431-112">A primeira mensagem na categoria de exibição seguinte se esse sinalizador **for OR** com VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="b8431-112">The first message in the next view category if this flag is **OR** ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="b8431-113">A última mensagem na categoria de exibição anterior se esse sinalizador for **OR** com VCDIR_PREV e a categoria anterior for expandida.</span><span class="sxs-lookup"><span data-stu-id="b8431-113">The last message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="b8431-114">A primeira mensagem na categoria de exibição anterior se esse sinalizador for **OR** com VCDIR_PREV e a categoria anterior não for expandida.</span><span class="sxs-lookup"><span data-stu-id="b8431-114">The first message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="b8431-115">Nesse caso, a categoria anterior passa por expansão automática.</span><span class="sxs-lookup"><span data-stu-id="b8431-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="b8431-116">VCDIR_DELETE: o visualizador deve ativar a mensagem seguinte ou anterior porque a mensagem atual foi excluída.</span><span class="sxs-lookup"><span data-stu-id="b8431-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="b8431-117">VCDIR_MOVE: o visualizador deve ativar a mensagem seguinte ou anterior porque a mensagem atual foi movida.</span><span class="sxs-lookup"><span data-stu-id="b8431-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="b8431-118">VCDIR_NEXT: o visualizador deve ativar a próxima mensagem na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8431-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="b8431-119">VCDIR_PREV: o visualizador deve ativar a mensagem anterior na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8431-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="b8431-120">VCDIR_UNREAD: o visualizador deve ativar a próxima mensagem não lida ou anterior na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8431-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="b8431-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="b8431-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="b8431-122">[in] Ponteiro para uma estrutura **de RECT** do Windows que contém o tamanho e a posição da janela a ser usada para exibir a mensagem ativada.</span><span class="sxs-lookup"><span data-stu-id="b8431-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b8431-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8431-123">Return value</span></span>

<span data-ttu-id="b8431-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8431-124">S_OK</span></span> 
  
> <span data-ttu-id="b8431-125">A mensagem foi ativada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b8431-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="b8431-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b8431-126">S_FALSE</span></span> 
  
> <span data-ttu-id="b8431-127">A mensagem foi ativada com êxito, mas um tipo diferente de formulário foi aberto no processo.</span><span class="sxs-lookup"><span data-stu-id="b8431-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8431-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8431-128">Remarks</span></span>

<span data-ttu-id="b8431-129">Os objetos de formulário chamam **o método IMAPIViewContext::ActivateNext** para alterar a mensagem exibida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b8431-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="b8431-130">O valor passado no  _parâmetro ulDir_ indica qual mensagem deve ser ativada e, em alguns casos, por quê.</span><span class="sxs-lookup"><span data-stu-id="b8431-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="b8431-131">Os VCDIR_NEXT e VCDIR_PREVIOUS de comando correspondem aos usuários escolhendo  o comando **Próximo** ou Anterior em um visualização, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b8431-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="b8431-132">Essas operações geralmente correspondem a mover para cima ou para baixo uma mensagem na lista de mensagens do visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="b8431-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="b8431-133">Os sinalizadores VCDIR_DELETE e VCDIR_MOVE são definidos pelos métodos [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) e [IMAPIMessageSite::MoveMessage,](imapimessagesite-movemessage.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b8431-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="b8431-134">As implementações desses métodos chamam **ActivateNext** com a direção apropriada e, em seguida, executam a operação solicitada na mensagem se a chamada **ActivateNext** não falhar.</span><span class="sxs-lookup"><span data-stu-id="b8431-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="b8431-135">Visualizadores de formulário normalmente permitem que os usuários especifiquem a direção para mover na lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b8431-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b8431-136">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b8431-136">Notes to implementers</span></span>

<span data-ttu-id="b8431-137">Sua implementação de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) faz a mensagem seguinte ou anterior na pasta, dependendo do valor de  _ulDir_, a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="b8431-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="b8431-138">Depois **que ActivateNext** retornar, chame [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obter um ponteiro para a mensagem recém-ativada.</span><span class="sxs-lookup"><span data-stu-id="b8431-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b8431-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b8431-139">Notes to callers</span></span>

<span data-ttu-id="b8431-140">Se **ActivateNext** retornar S_FALSE, ou se uma mensagem atual não estiver presente, execute o procedimento de desligamento normal, que deve incluir chamar o método [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) do formulário.</span><span class="sxs-lookup"><span data-stu-id="b8431-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="b8431-141">Se uma mensagem seguinte ou anterior for exibida, use o retângulo de janela passado no parâmetro  _prcPosRect_ para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="b8431-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8431-142">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8431-142">MFCMAPI reference</span></span>

<span data-ttu-id="b8431-143">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8431-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8431-144">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b8431-144">**File**</span></span>|<span data-ttu-id="b8431-145">**Função**</span><span class="sxs-lookup"><span data-stu-id="b8431-145">**Function**</span></span>|<span data-ttu-id="b8431-146">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b8431-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8431-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b8431-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b8431-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="b8431-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="b8431-149">MFCMAPI implementa o **método IMAPIViewContext::ActivateNext** nesta função.</span><span class="sxs-lookup"><span data-stu-id="b8431-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8431-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8431-150">See also</span></span>

- [<span data-ttu-id="b8431-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="b8431-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="b8431-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8431-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="b8431-153">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b8431-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

