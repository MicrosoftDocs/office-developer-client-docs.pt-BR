---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321410"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="ab6d2-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="ab6d2-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="ab6d2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab6d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab6d2-105">Exclui a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="ab6d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab6d2-106">Parameters</span></span>

 <span data-ttu-id="ab6d2-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="ab6d2-107">_pViewContext_</span></span>
  
> <span data-ttu-id="ab6d2-108">no Um ponteiro para um objeto de contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="ab6d2-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="ab6d2-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="ab6d2-110">no Um ponteiro para uma estrutura de [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário atual.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="ab6d2-111">O próximo formulário também usa este retângulo de janela.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab6d2-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ab6d2-112">Return value</span></span>

<span data-ttu-id="ab6d2-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab6d2-113">S_OK</span></span> 
  
> <span data-ttu-id="ab6d2-114">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ab6d2-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ab6d2-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ab6d2-116">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab6d2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab6d2-117">Remarks</span></span>

<span data-ttu-id="ab6d2-118">Um objeto Form chama o método **IMAPIMessageSite::D eletemessage** para excluir a mensagem que o formulário está exibindo no momento.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab6d2-119">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ab6d2-119">Notes to callers</span></span>

<span data-ttu-id="ab6d2-120">Após o retorno de **DeleteMessage**, os objetos Form devem verificar uma nova mensagem e, em seguida, se não houver nenhum.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="ab6d2-121">Para determinar se a mensagem **DeleteMessage** atuou em foi excluída ou movida para uma pasta **itens excluídos** , um objeto Form pode chamar o método [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar se o sinalizador DELETE_IS_MOVE foi retornado.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ab6d2-122">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ab6d2-122">Notes to implementers</span></span>

<span data-ttu-id="ab6d2-123">Se a implementação de um visualizador de formulários do método **DeleteMessage** for movida para a próxima mensagem depois de excluir uma mensagem, a implementação deverá chamar o método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) e passar o sinalizador VCDIR_DELETE antes de executar a exclusão real.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="ab6d2-124">Se a implementação de um visualizador de formulários do **DeleteMessage** mover a mensagem excluída (por exemplo, para uma pasta **itens excluídos** ), a implementação deverá salvar as alterações na mensagem se a mensagem tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="ab6d2-125">Uma implementação típica do **DeleteMessage** realiza as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="ab6d2-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="ab6d2-126">Se a implementação estiver movendo a mensagem, ela chamará o método [IPersistMessage:: Save](ipersistmessage-save.md) , passando **NULL** no parâmetro _PMessage_ e **true** no parâmetro _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="ab6d2-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="ab6d2-127">Ele chama o método **IMAPIViewContext:: ActivateNext** , passando o sinalizador VCDIR_DELETE no parâmetro _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="ab6d2-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="ab6d2-128">Se a chamada **ActivateNext** falhar, ela retornará.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="ab6d2-129">Se **ActivateNext** retornar S_FALSE, ele chamará o método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6d2-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="ab6d2-130">Ele exclui ou move a mensagem.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="ab6d2-131">Para obter a estrutura do **Rect** usada pela janela de um formulário, chame a função [GetWindowRect](https://msdn.microsoft.com/library/ms633519) do Windows.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="ab6d2-132">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ab6d2-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ab6d2-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ab6d2-133">MFCMAPI reference</span></span>

<span data-ttu-id="ab6d2-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ab6d2-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ab6d2-135">**File**</span></span>|<span data-ttu-id="ab6d2-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="ab6d2-136">**Function**</span></span>|<span data-ttu-id="ab6d2-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ab6d2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab6d2-138">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="ab6d2-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ab6d2-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="ab6d2-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="ab6d2-140">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="ab6d2-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab6d2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab6d2-141">See also</span></span>



[<span data-ttu-id="ab6d2-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="ab6d2-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="ab6d2-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ab6d2-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="ab6d2-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="ab6d2-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="ab6d2-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="ab6d2-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="ab6d2-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab6d2-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="ab6d2-147">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ab6d2-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ab6d2-148">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="ab6d2-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

