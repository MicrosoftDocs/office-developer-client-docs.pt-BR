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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351153"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="ae75d-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ae75d-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="ae75d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae75d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae75d-105">Ativa a mensagem seguinte ou anterior no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae75d-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="ae75d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae75d-106">Parameters</span></span>

<span data-ttu-id="ae75d-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="ae75d-107">_ulDir_</span></span>
  
> <span data-ttu-id="ae75d-108">no Sinalizadores de status fornecendo informações sobre a mensagem a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="ae75d-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="ae75d-109">As configurações de sinalizador válidas são:</span><span class="sxs-lookup"><span data-stu-id="ae75d-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="ae75d-110">VCDIR_CATEGORY: o visualizador deve ativar uma mensagem em outra categoria do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae75d-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="ae75d-111">A mensagem a ser ativada é:</span><span class="sxs-lookup"><span data-stu-id="ae75d-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="ae75d-112">A primeira mensagem na próxima categoria de exibição se esse sinalizador estiver **ou**Ed com VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="ae75d-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="ae75d-113">A última mensagem na categoria modo de exibição anterior se esse sinalizador estiver **ou**Ed com VCDIR_PREV e a categoria anterior estiver expandida.</span><span class="sxs-lookup"><span data-stu-id="ae75d-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="ae75d-114">A primeira mensagem na categoria modo de exibição anterior se esse sinalizador for **ou**Ed com VCDIR_PREV e a categoria anterior não estiver expandida.</span><span class="sxs-lookup"><span data-stu-id="ae75d-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="ae75d-115">Nesse caso, a categoria anterior passa pela expansão automática.</span><span class="sxs-lookup"><span data-stu-id="ae75d-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="ae75d-116">VCDIR_DELETE: o visualizador deve ativar a mensagem seguinte ou anterior porque a mensagem atual foi excluída.</span><span class="sxs-lookup"><span data-stu-id="ae75d-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="ae75d-117">VCDIR_MOVE: o visualizador deve ativar a mensagem seguinte ou anterior porque a mensagem atual foi movida.</span><span class="sxs-lookup"><span data-stu-id="ae75d-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="ae75d-118">VCDIR_NEXT: o visualizador deve ativar a próxima mensagem na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae75d-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="ae75d-119">VCDIR_PREV: o visualizador deve ativar a mensagem anterior na ordem de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae75d-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="ae75d-120">VCDIR_UNREAD: o visualizador deve ativar a mensagem não lida seguinte ou anterior no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae75d-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="ae75d-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="ae75d-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="ae75d-122">no Ponteiro para uma estrutura de **Rect** do Windows contendo o tamanho e a posição da janela a ser usada para exibir a mensagem ativada.</span><span class="sxs-lookup"><span data-stu-id="ae75d-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ae75d-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ae75d-123">Return value</span></span>

<span data-ttu-id="ae75d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae75d-124">S_OK</span></span> 
  
> <span data-ttu-id="ae75d-125">A mensagem foi ativada com êxito.</span><span class="sxs-lookup"><span data-stu-id="ae75d-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="ae75d-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ae75d-126">S_FALSE</span></span> 
  
> <span data-ttu-id="ae75d-127">A mensagem foi ativada com êxito, mas um tipo diferente de formulário foi aberto no processo.</span><span class="sxs-lookup"><span data-stu-id="ae75d-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae75d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae75d-128">Remarks</span></span>

<span data-ttu-id="ae75d-129">Os objetos Form chamam o método **IMAPIViewContext:: ActivateNext** para alterar qual mensagem é exibida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ae75d-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="ae75d-130">O valor passado no parâmetro _ulDir_ indica qual mensagem deve ser ativada e, em alguns casos, por quê.</span><span class="sxs-lookup"><span data-stu-id="ae75d-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="ae75d-131">Os sinalizadores VCDIR_NEXT e VCDIR_PREVIOUS correspondem aos usuários que escolhem o comando **próximo** ou **anterior** em um modo de exibição, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ae75d-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="ae75d-132">Essas operações geralmente correspondem à movimentação de uma mensagem para cima ou para baixo na lista de mensagens do Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="ae75d-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="ae75d-133">Os sinalizadores VCDIR_DELETE e VCDIR_MOVE são definidos pelos métodos [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) e [IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ae75d-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="ae75d-134">As implementações desses métodos chamam **ActivateNext** com a direção apropriada e, em seguida, executam a operação solicitada na mensagem se a chamada **ActivateNext** não falhar.</span><span class="sxs-lookup"><span data-stu-id="ae75d-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="ae75d-135">Geralmente, os visualizadores de formulários permitem que os usuários especifiquem a direção da movimentação na lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ae75d-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ae75d-136">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ae75d-136">Notes to implementers</span></span>

<span data-ttu-id="ae75d-137">Sua implementação do [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) faz a mensagem seguinte ou anterior na pasta, dependendo do valor de _ulDir_, a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="ae75d-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="ae75d-138">Após o **ActivateNext** retornar, chame [IMAPIMessageSite:: GetMessage](imapimessagesite-getmessage.md) para obter um ponteiro para a mensagem recentemente ativada.</span><span class="sxs-lookup"><span data-stu-id="ae75d-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ae75d-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ae75d-139">Notes to callers</span></span>

<span data-ttu-id="ae75d-140">Se **ActivateNext** retornar S_FALSE, ou se uma mensagem atual não estiver presente, execute o procedimento de desligamento normal que deve incluir a chamada do método [IMAPIForm:: ShutdownForm](imapiform-shutdownform.md) do seu formulário.</span><span class="sxs-lookup"><span data-stu-id="ae75d-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="ae75d-141">Se uma mensagem seguinte ou anterior for exibida, use o retângulo da janela passado no parâmetro _prcPosRect_ para exibi-la.</span><span class="sxs-lookup"><span data-stu-id="ae75d-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ae75d-142">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ae75d-142">MFCMAPI reference</span></span>

<span data-ttu-id="ae75d-143">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae75d-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ae75d-144">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ae75d-144">**File**</span></span>|<span data-ttu-id="ae75d-145">**Função**</span><span class="sxs-lookup"><span data-stu-id="ae75d-145">**Function**</span></span>|<span data-ttu-id="ae75d-146">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ae75d-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae75d-147">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="ae75d-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ae75d-148">CMyMAPIFormViewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ae75d-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="ae75d-149">MFCMAPI implementa o método **IMAPIViewContext:: ActivateNext** nesta função.</span><span class="sxs-lookup"><span data-stu-id="ae75d-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae75d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae75d-150">See also</span></span>

- [<span data-ttu-id="ae75d-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="ae75d-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="ae75d-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae75d-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="ae75d-153">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ae75d-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

