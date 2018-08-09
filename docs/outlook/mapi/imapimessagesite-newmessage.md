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
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767093"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="c8a0d-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="c8a0d-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="c8a0d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8a0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8a0d-105">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="c8a0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8a0d-106">Parameters</span></span>

 <span data-ttu-id="c8a0d-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="c8a0d-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="c8a0d-108">[in] Indica a mensagem na pasta na qual deve ser composta.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="c8a0d-109">Se a variável for FALSE, o parâmetro _pFolderFocus_ será ignorado e a tela de formulário pode escreva a mensagem em qualquer pasta.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="c8a0d-110">Se a variável é TRUE e NULL é passada no parâmetro _pFolderFocus_ , a mensagem é composta na pasta atual.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="c8a0d-111">Se a variável for TRUE e um valor de não-nulo é transmitido em _pFolderFocus_, a mensagem é composta na pasta indicada por _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="c8a0d-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="c8a0d-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="c8a0d-113">[in] Um ponteiro para a pasta onde a nova mensagem é criada.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="c8a0d-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="c8a0d-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="c8a0d-115">[in] Um ponteiro para o objeto de formulário para o novo formulário.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="c8a0d-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="c8a0d-116">_ppMessage_</span></span>
  
> <span data-ttu-id="c8a0d-117">[out] Um ponteiro para um ponteiro para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="c8a0d-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="c8a0d-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="c8a0d-119">[out] Um ponteiro para um ponteiro para um objeto de site de mensagem da nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="c8a0d-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="c8a0d-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="c8a0d-121">[out] Um ponteiro para um ponteiro para um contexto de modo de exibição que é apropriado para passagem para um novo formulário com a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="c8a0d-122">Se o formulário implementa seu próprio contexto de modo de exibição, NULL pode ser passado no parâmetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="c8a0d-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8a0d-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c8a0d-123">Return value</span></span>

<span data-ttu-id="c8a0d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8a0d-124">S_OK</span></span> 
  
> <span data-ttu-id="c8a0d-125">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8a0d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8a0d-126">Remarks</span></span>

<span data-ttu-id="c8a0d-127">Objetos de formulário chame o método **IMAPIMessageSite::NewMessage** para criar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="c8a0d-128">O formulário usa **NewMessage** para fazer uma nova mensagem e o site de mensagem associada a partir de seu modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="c8a0d-129">Em seguida, ele pode modificar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="c8a0d-130">Você também pode obter um contexto de modo de exibição associado, passando um valor nulo no parâmetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="c8a0d-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="c8a0d-131">Nesse contexto de modo de exibição pode ser usado diretamente, ou podem ser agregado e passado para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="c8a0d-132">Se uma implementação completa for necessária, passe NULL no _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="c8a0d-133">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c8a0d-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8a0d-134">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c8a0d-134">MFCMAPI reference</span></span>

<span data-ttu-id="c8a0d-135">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8a0d-136">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c8a0d-136">**File**</span></span>|<span data-ttu-id="c8a0d-137">**Function**</span><span class="sxs-lookup"><span data-stu-id="c8a0d-137">**Function**</span></span>|<span data-ttu-id="c8a0d-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c8a0d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8a0d-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c8a0d-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c8a0d-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="c8a0d-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="c8a0d-141">MFCMAPI usa o método **IMAPIMessageSite::NewMessage** para criar uma nova mensagem, instanciar um novo Visualizador de formulário e chamar **SetPersist** para definir a mensagem no Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="c8a0d-142">Finalmente, ela retornará o Visualizador do formulário como o site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8a0d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8a0d-143">See also</span></span>



[<span data-ttu-id="c8a0d-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8a0d-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="c8a0d-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8a0d-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c8a0d-146">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c8a0d-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c8a0d-147">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="c8a0d-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

