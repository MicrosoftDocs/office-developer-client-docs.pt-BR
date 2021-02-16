---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418782"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="a18f3-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="a18f3-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="a18f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a18f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a18f3-105">Inicia um formulário para abrir uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="a18f3-105">Starts a form to open an existing message.</span></span>
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="a18f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a18f3-106">Parameters</span></span>

 <span data-ttu-id="a18f3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a18f3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a18f3-108">[in] Um alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="a18f3-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="a18f3-109">O _parâmetro ulUIParam é_ ignorado, a menos que o MAPI_DIALOG padrão seja definido no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a18f3-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a18f3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a18f3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a18f3-111">[in] Uma máscara de bits de sinalizadores que controla como o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="a18f3-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="a18f3-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a18f3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="a18f3-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a18f3-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a18f3-114">Exibe uma interface do usuário para fornecer status ou solicitar ao usuário mais informações.</span><span class="sxs-lookup"><span data-stu-id="a18f3-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="a18f3-115">Se esse sinalizador não estiver definido, nenhuma interface do usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="a18f3-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="a18f3-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a18f3-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a18f3-117">Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="a18f3-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a18f3-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a18f3-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="a18f3-119">[in] Um ponteiro para uma cadeia de caracteres que nomeia a classe de mensagem da mensagem a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="a18f3-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="a18f3-120">Se NULL for passado no parâmetro _lpszMessageClass,_ a classe de mensagem será determinada a partir da mensagem apontada pelo _parâmetro pmsg._</span><span class="sxs-lookup"><span data-stu-id="a18f3-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="a18f3-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="a18f3-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="a18f3-122">[in] Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem que fornece informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="a18f3-123">O  _parâmetro ulMessageStatus_ deve ser definido se  _lpszMessageClass_ for non-NULL; caso contrário,  _ulMessageStatus_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a18f3-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="a18f3-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="a18f3-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="a18f3-125">[in] Um ponteiro para uma máscara de bits de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem que indica o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="a18f3-126">O  _parâmetro ulMessageFlags_ deve ser definido se  _lpszMessageClass_ for non-NULL; caso contrário,  _ulMessageFlags_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a18f3-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="a18f3-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="a18f3-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="a18f3-128">[in] Um ponteiro para a pasta que contém diretamente a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="a18f3-129">O  _parâmetro pFolderFocus_ poderá ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada em outra mensagem).</span><span class="sxs-lookup"><span data-stu-id="a18f3-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="a18f3-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="a18f3-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="a18f3-131">[in] Um ponteiro para o site de mensagens da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="a18f3-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="a18f3-132">_pmsg_</span></span>
  
> <span data-ttu-id="a18f3-133">[in] Um ponteiro para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="a18f3-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="a18f3-134">_pViewContext_</span></span>
  
> <span data-ttu-id="a18f3-135">[in] Um ponteiro para o contexto de exibição da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="a18f3-136">O  _parâmetro pViewContext_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a18f3-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a18f3-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="a18f3-137">_riid_</span></span>
  
> <span data-ttu-id="a18f3-138">[in] O IID (identificador de interface) da interface a ser usada para o objeto de formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="a18f3-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="a18f3-139">O  _parâmetro riid_ não deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a18f3-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="a18f3-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="a18f3-140">_ppvObj_</span></span>
  
> <span data-ttu-id="a18f3-141">[out] Um ponteiro para um ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="a18f3-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a18f3-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a18f3-142">Return value</span></span>

<span data-ttu-id="a18f3-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="a18f3-143">S_OK</span></span> 
  
> <span data-ttu-id="a18f3-144">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a18f3-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a18f3-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a18f3-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="a18f3-146">O formulário não dá suporte à interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="a18f3-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="a18f3-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a18f3-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a18f3-148">A classe de mensagem passada  _em lpszMessageClass_ não combina com a classe de mensagem de nenhum formulário na biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="a18f3-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a18f3-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="a18f3-149">Remarks</span></span>

<span data-ttu-id="a18f3-150">Visualizadores de formulário chamam **o método IMAPIFormMgr::LoadForm** para abrir um formulário para uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="a18f3-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="a18f3-151">**LoadForm** abre o objeto de formulário, carrega a mensagem no objeto de formulário, configura o contexto de exibição apropriado, se necessário, e retorna a interface solicitada para o objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="a18f3-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="a18f3-152">O  _parâmetro pFolderFocus_ aponta para a pasta que contém a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="a18f3-153">Se a mensagem estiver incorporada em outra mensagem,  _pFolderFocus_ deverá ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a18f3-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a18f3-154">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="a18f3-154">Notes to implementers</span></span>

<span data-ttu-id="a18f3-155">Se NULL for passado em  _lpszMessageClass_, a implementação obterá a classe de mensagem, o status e os sinalizadores da mensagem das propriedades **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** e **PR_MESSAGE_FLAGS** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a18f3-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="a18f3-156">Se uma cadeia de caracteres de classe de mensagem for fornecida em  _lpszMessageClass_, a implementação deverá usar os valores em  _ulMessageStatus_ e  _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="a18f3-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a18f3-157">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a18f3-157">MFCMAPI reference</span></span>

<span data-ttu-id="a18f3-158">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a18f3-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a18f3-159">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a18f3-159">**File**</span></span>|<span data-ttu-id="a18f3-160">**Função**</span><span class="sxs-lookup"><span data-stu-id="a18f3-160">**Function**</span></span>|<span data-ttu-id="a18f3-161">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="a18f3-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a18f3-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a18f3-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a18f3-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="a18f3-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="a18f3-164">MFCMAPI usa o **método IMAPIFormMgr::LoadForm** para carregar um formulário antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="a18f3-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a18f3-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="a18f3-165">See also</span></span>



[<span data-ttu-id="a18f3-166">Propriedade canônica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="a18f3-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="a18f3-167">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="a18f3-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="a18f3-168">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a18f3-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="a18f3-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a18f3-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="a18f3-170">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a18f3-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

