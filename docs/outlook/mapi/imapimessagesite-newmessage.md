---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438768"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="4d6f3-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="4d6f3-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="4d6f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d6f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d6f3-105">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="4d6f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d6f3-106">Parameters</span></span>

 <span data-ttu-id="4d6f3-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="4d6f3-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="4d6f3-108">no Indica em qual pasta a mensagem deve ser redigida.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="4d6f3-109">Se a variável for FALSE, o parâmetro _pFolderFocus_ será ignorado e o Visualizador de formulários poderá redigir a mensagem em qualquer pasta.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="4d6f3-110">Se a variável for TRUE e NULL for passado no parâmetro _pFolderFocus_ , a mensagem será composta na pasta atual.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="4d6f3-111">Se a variável for TRUE e um valor não nulo for passado em _pFolderFocus_, a mensagem será composta na pasta indicada por _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="4d6f3-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="4d6f3-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="4d6f3-113">no Um ponteiro para a pasta onde a nova mensagem é criada.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="4d6f3-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="4d6f3-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="4d6f3-115">no Um ponteiro para o objeto Form para o novo formulário.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="4d6f3-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="4d6f3-116">_ppMessage_</span></span>
  
> <span data-ttu-id="4d6f3-117">bota Um ponteiro para um ponteiro para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="4d6f3-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="4d6f3-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="4d6f3-119">bota Um ponteiro para um ponteiro para um objeto de site de mensagem para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="4d6f3-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="4d6f3-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="4d6f3-121">bota Um ponteiro para um ponteiro para um contexto de exibição que é apropriado para passar para um novo formulário com a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="4d6f3-122">Se o formulário implementar seu próprio contexto de exibição, NULL pode ser passado no parâmetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="4d6f3-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d6f3-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4d6f3-123">Return value</span></span>

<span data-ttu-id="4d6f3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d6f3-124">S_OK</span></span> 
  
> <span data-ttu-id="4d6f3-125">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d6f3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d6f3-126">Remarks</span></span>

<span data-ttu-id="4d6f3-127">Os objetos Form chamam o método **IMAPIMessageSite:: NewMessage** para criar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="4d6f3-128">O formulário usa **NewMessage** para obter uma nova mensagem e o site de mensagem associado de seu modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="4d6f3-129">Em seguida, ele pode modificar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="4d6f3-130">Você também pode obter um contexto de exibição associado passando um valor não nulo no parâmetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="4d6f3-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="4d6f3-131">Este contexto de exibição pode ser usado diretamente ou pode ser agregado e transmitido para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="4d6f3-132">Se for necessária uma implementação completa, passe NULL no _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="4d6f3-133">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4d6f3-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4d6f3-134">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4d6f3-134">MFCMAPI reference</span></span>

<span data-ttu-id="4d6f3-135">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4d6f3-136">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4d6f3-136">**File**</span></span>|<span data-ttu-id="4d6f3-137">**Função**</span><span class="sxs-lookup"><span data-stu-id="4d6f3-137">**Function**</span></span>|<span data-ttu-id="4d6f3-138">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="4d6f3-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d6f3-139">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="4d6f3-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="4d6f3-140">CMyMAPIFormViewer:: NewMessage</span><span class="sxs-lookup"><span data-stu-id="4d6f3-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="4d6f3-141">MFCMAPI usa o método **IMAPIMessageSite:: NewMessage** para criar uma nova mensagem, criar uma instância de um novo Visualizador de \*\*\*\* formulários e chamar setpersist para definir a mensagem no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="4d6f3-142">Por fim, ele retorna o Visualizador de formulários como o site de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d6f3-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d6f3-143">See also</span></span>



[<span data-ttu-id="4d6f3-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d6f3-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="4d6f3-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d6f3-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="4d6f3-146">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4d6f3-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4d6f3-147">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="4d6f3-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

