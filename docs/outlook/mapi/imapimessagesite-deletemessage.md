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
ms.openlocfilehash: 6ed73cd683f1668900a76f7b8c48494952e9fc14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573345"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="7ca0d-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="7ca0d-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="7ca0d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ca0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ca0d-105">Exclui a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="7ca0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ca0d-106">Parameters</span></span>

 <span data-ttu-id="7ca0d-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="7ca0d-107">_pViewContext_</span></span>
  
> <span data-ttu-id="7ca0d-108">[in] Um ponteiro para um objeto de contexto do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="7ca0d-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="7ca0d-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="7ca0d-110">[in] Um ponteiro para uma estrutura de [Retangular](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contém o tamanho da janela e a posição atual do formulário.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-110">[in] A pointer to a [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="7ca0d-111">A próxima forma exibida também usa esse retângulo de janela.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7ca0d-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7ca0d-112">Return value</span></span>

<span data-ttu-id="7ca0d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ca0d-113">S_OK</span></span> 
  
> <span data-ttu-id="7ca0d-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7ca0d-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7ca0d-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7ca0d-116">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ca0d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ca0d-117">Remarks</span></span>

<span data-ttu-id="7ca0d-118">Um objeto form chama o método **IMAPIMessageSite::DeleteMessage** para excluir a mensagem que o formulário está exibindo no momento.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7ca0d-119">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7ca0d-119">Notes to callers</span></span>

<span data-ttu-id="7ca0d-120">Após o retorno de **DeleteMessage**, os objetos de formulário devem verificar se há uma nova mensagem e, em seguida, descartar sozinhos, se não houver nenhum.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="7ca0d-121">Para determinar se a mensagem **que deletemessage** realizadas foi excluída ou movida para uma pasta de **Itens excluídos** , um objeto form pode chamar o método [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar se o sinalizador DELETE_IS_MOVE foi retornado.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7ca0d-122">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="7ca0d-122">Notes to implementers</span></span>

<span data-ttu-id="7ca0d-123">Se a implementação do Visualizador de um formulário do método **DeleteMessage** move para a próxima mensagem após ela exclui uma mensagem, a implementação deve chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) e passar o sinalizador VCDIR_DELETE antes de executar a exclusão real.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="7ca0d-124">Se a implementação do Visualizador de um formulário de **DeleteMessage** move a mensagem excluída (por exemplo, para uma pasta de **Itens excluídos** ), a implementação deve salvar alterações na mensagem se a mensagem foi modificada.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="7ca0d-125">Uma implementação típica de **DeleteMessage** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="7ca0d-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="7ca0d-126">Se a mensagem está se movendo a implementação, ele chama o método [IPersistMessage::Save](ipersistmessage-save.md) , passando **null** no parâmetro _pMessage_ e **true** no parâmetro _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="7ca0d-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="7ca0d-127">Ele chama o método **IMAPIViewContext::ActivateNext** , passando o sinalizador VCDIR_DELETE no parâmetro _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="7ca0d-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="7ca0d-128">Se a chamada **ActivateNext** falha, será retornado.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="7ca0d-129">Se **ActivateNext** retornar S_FALSE, ele chama o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca0d-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="7ca0d-130">Exclui ou move a mensagem.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="7ca0d-131">Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função do Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="7ca0d-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="7ca0d-132">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7ca0d-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ca0d-133">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7ca0d-133">MFCMAPI reference</span></span>

<span data-ttu-id="7ca0d-134">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ca0d-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-135">**File**</span></span>|<span data-ttu-id="7ca0d-136">**Function**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-136">**Function**</span></span>|<span data-ttu-id="7ca0d-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ca0d-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7ca0d-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7ca0d-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="7ca0d-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="7ca0d-140">Não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ca0d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ca0d-141">See also</span></span>



[<span data-ttu-id="7ca0d-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="7ca0d-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="7ca0d-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="7ca0d-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="7ca0d-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="7ca0d-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="7ca0d-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="7ca0d-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="7ca0d-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ca0d-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="7ca0d-147">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7ca0d-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7ca0d-148">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="7ca0d-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

