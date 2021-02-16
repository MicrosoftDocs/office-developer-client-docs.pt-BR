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
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="468fd-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="468fd-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="468fd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="468fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="468fd-105">Exclui a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="468fd-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="468fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="468fd-106">Parameters</span></span>

 <span data-ttu-id="468fd-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="468fd-107">_pViewContext_</span></span>
  
> <span data-ttu-id="468fd-108">[in] Um ponteiro para um objeto de contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="468fd-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="468fd-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="468fd-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="468fd-110">[in] Um ponteiro para uma [estrutura RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário atual.</span><span class="sxs-lookup"><span data-stu-id="468fd-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="468fd-111">O próximo formulário exibido também usa esse retângulo de janela.</span><span class="sxs-lookup"><span data-stu-id="468fd-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="468fd-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="468fd-112">Return value</span></span>

<span data-ttu-id="468fd-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="468fd-113">S_OK</span></span> 
  
> <span data-ttu-id="468fd-114">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="468fd-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="468fd-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="468fd-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="468fd-116">A operação não é suportada por este site de mensagens.</span><span class="sxs-lookup"><span data-stu-id="468fd-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="468fd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="468fd-117">Remarks</span></span>

<span data-ttu-id="468fd-118">Um objeto de formulário chama o **método IMAPIMessageSite::D eleteMessage** para excluir a mensagem que o formulário está exibindo no momento.</span><span class="sxs-lookup"><span data-stu-id="468fd-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="468fd-119">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="468fd-119">Notes to callers</span></span>

<span data-ttu-id="468fd-120">Após o retorno de **DeleteMessage**, os objetos de formulário devem verificar se há uma nova mensagem e, em seguida, descartar a si mesmos se não existe.</span><span class="sxs-lookup"><span data-stu-id="468fd-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="468fd-121">Para determinar se **a** mensagem em que **DeleteMessage** atuou foi excluída ou movida para uma pasta Itens Excluídos, um objeto de formulário pode chamar o método [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar se o sinalizador DELETE_IS_MOVE foi retornado.</span><span class="sxs-lookup"><span data-stu-id="468fd-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="468fd-122">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="468fd-122">Notes to implementers</span></span>

<span data-ttu-id="468fd-123">Se a implementação do método **DeleteMessage** de um visualizador de formulário for para a próxima mensagem depois de excluir uma mensagem, a implementação deverá chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) e passar o sinalizador VCDIR_DELETE antes de executar a exclusão real.</span><span class="sxs-lookup"><span data-stu-id="468fd-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="468fd-124">Se a implementação de **DeleteMessage** de um visualizador de formulário mover **a** mensagem excluída (por exemplo, para uma pasta Itens Excluídos), a implementação deverá salvar as alterações na mensagem se a mensagem tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="468fd-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="468fd-125">Uma implementação típica **de DeleteMessage** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="468fd-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="468fd-126">Se a implementação estiver movendo a mensagem, ela chamará o método [IPersistMessage::Save,](ipersistmessage-save.md) passando **nulo** no parâmetro _pMessage_ e **true** no parâmetro _fSameAsLoad._</span><span class="sxs-lookup"><span data-stu-id="468fd-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="468fd-127">Ele chama o **método IMAPIViewContext::ActivateNext,** passando o VCDIR_DELETE de texto no _parâmetro ulDir._</span><span class="sxs-lookup"><span data-stu-id="468fd-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="468fd-128">Se a **chamada ActivateNext** falhar, ela retornará.</span><span class="sxs-lookup"><span data-stu-id="468fd-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="468fd-129">Se **ActivateNext** retornar S_FALSE, ele chamará o [método IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md)</span><span class="sxs-lookup"><span data-stu-id="468fd-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="468fd-130">Ele exclui ou move a mensagem.</span><span class="sxs-lookup"><span data-stu-id="468fd-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="468fd-131">Para obter a **estrutura RECT** usada pela janela de um formulário, chame a função [Windows GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="468fd-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="468fd-132">Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="468fd-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="468fd-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="468fd-133">MFCMAPI reference</span></span>

<span data-ttu-id="468fd-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="468fd-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="468fd-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="468fd-135">**File**</span></span>|<span data-ttu-id="468fd-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="468fd-136">**Function**</span></span>|<span data-ttu-id="468fd-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="468fd-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="468fd-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="468fd-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="468fd-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="468fd-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="468fd-140">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="468fd-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="468fd-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="468fd-141">See also</span></span>



[<span data-ttu-id="468fd-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="468fd-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="468fd-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="468fd-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="468fd-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="468fd-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="468fd-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="468fd-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="468fd-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="468fd-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="468fd-147">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="468fd-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="468fd-148">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="468fd-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

