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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321685"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="2ae49-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="2ae49-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="2ae49-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ae49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ae49-105">Inicia um formulário para abrir uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="2ae49-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2ae49-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ae49-106">Parameters</span></span>

 <span data-ttu-id="2ae49-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2ae49-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="2ae49-108">no Uma alça para a janela pai do indicador de progresso exibida enquanto o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="2ae49-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="2ae49-109">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="2ae49-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2ae49-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ae49-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2ae49-111">no Uma bitmask de sinalizadores que controla como o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="2ae49-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="2ae49-112">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="2ae49-112">The following flags can be set:</span></span>
    
<span data-ttu-id="2ae49-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2ae49-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="2ae49-114">Exibe uma interface do usuário para fornecer status ou solicitar mais informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2ae49-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="2ae49-115">Se esse sinalizador não for definido, nenhuma interface de usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="2ae49-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="2ae49-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="2ae49-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="2ae49-117">Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="2ae49-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="2ae49-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="2ae49-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="2ae49-119">no Um ponteiro para uma cadeia de caracteres que nomeia a classe da mensagem a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="2ae49-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="2ae49-120">Se NULL for passado no parâmetro _lpszMessageClass_ , a classe Message será determinada da mensagem indicada pelo parâmetro _pMsg_ .</span><span class="sxs-lookup"><span data-stu-id="2ae49-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="2ae49-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="2ae49-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="2ae49-122">no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem que fornece informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="2ae49-123">O parâmetro _ulMessageStatus_ deve ser definido se _LPSZMESSAGECLASS_ for não nulo; caso contrário, _ulMessageStatus_ será ignorada.</span><span class="sxs-lookup"><span data-stu-id="2ae49-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="2ae49-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="2ae49-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="2ae49-125">no Um ponteiro para uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem que indica o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="2ae49-126">O parâmetro _ulMessageFlags_ deve ser definido se _LPSZMESSAGECLASS_ for não nulo; caso contrário, _ulMessageFlags_ será ignorada.</span><span class="sxs-lookup"><span data-stu-id="2ae49-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="2ae49-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="2ae49-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="2ae49-128">no Um ponteiro para a pasta que contém diretamente a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="2ae49-129">O parâmetro _pFolderFocus_ pode ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada a outra mensagem).</span><span class="sxs-lookup"><span data-stu-id="2ae49-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="2ae49-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="2ae49-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="2ae49-131">no Um ponteiro para o site de mensagens da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="2ae49-132">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="2ae49-132">_pmsg_</span></span>
  
> <span data-ttu-id="2ae49-133">no Um ponteiro para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="2ae49-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="2ae49-134">_pViewContext_</span></span>
  
> <span data-ttu-id="2ae49-135">no Um ponteiro para o contexto de exibição da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="2ae49-136">O parâmetro _pViewContext_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2ae49-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="2ae49-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="2ae49-137">_riid_</span></span>
  
> <span data-ttu-id="2ae49-138">no O identificador de interface (IID) da interface a ser usado para o objeto Form retornado.</span><span class="sxs-lookup"><span data-stu-id="2ae49-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="2ae49-139">O parâmetro _riid_ não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="2ae49-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="2ae49-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="2ae49-140">_ppvObj_</span></span>
  
> <span data-ttu-id="2ae49-141">bota Um ponteiro para um ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="2ae49-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ae49-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2ae49-142">Return value</span></span>

<span data-ttu-id="2ae49-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ae49-143">S_OK</span></span> 
  
> <span data-ttu-id="2ae49-144">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="2ae49-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2ae49-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="2ae49-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="2ae49-146">O formulário não dá suporte à interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="2ae49-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="2ae49-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2ae49-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2ae49-148">A classe de mensagens passada no _lpszMessageClass_ não corresponde à classe da mensagem de qualquer formulário na biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="2ae49-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2ae49-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ae49-149">Remarks</span></span>

<span data-ttu-id="2ae49-150">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: loadform** para abrir um formulário para uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="2ae49-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="2ae49-151">**Loadform** abre o objeto Form, carrega a mensagem no objeto Form, configura o contexto de exibição apropriado, se necessário, e retorna a interface solicitada para o objeto Form.</span><span class="sxs-lookup"><span data-stu-id="2ae49-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="2ae49-152">O parâmetro _pFolderFocus_ aponta para a pasta que contém a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ae49-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="2ae49-153">Se a mensagem for incorporada a outra mensagem, _pFolderFocus_ deverá ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2ae49-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2ae49-154">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="2ae49-154">Notes to implementers</span></span>

<span data-ttu-id="2ae49-155">Se NULL for passado no _lpszMessageClass_, a implementação obterá a classe de mensagem, o status e os sinalizadores da mensagem de **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** e \*\*PR_MESSAGE_FLAGS \*\*Propriedades.</span><span class="sxs-lookup"><span data-stu-id="2ae49-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="2ae49-156">Se uma cadeia de caracteres de classe de mensagem for fornecida no _lpszMessageClass_, a implementação deverá usar os valores em _ulMessageStatus_ e _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="2ae49-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ae49-157">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2ae49-157">MFCMAPI reference</span></span>

<span data-ttu-id="2ae49-158">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ae49-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ae49-159">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2ae49-159">**File**</span></span>|<span data-ttu-id="2ae49-160">**Função**</span><span class="sxs-lookup"><span data-stu-id="2ae49-160">**Function**</span></span>|<span data-ttu-id="2ae49-161">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="2ae49-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ae49-162">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="2ae49-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2ae49-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="2ae49-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2ae49-164">MFCMAPI usa o método **IMAPIFormMgr:: loadform** para carregar um formulário antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="2ae49-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ae49-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ae49-165">See also</span></span>



[<span data-ttu-id="2ae49-166">Propriedade canônica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="2ae49-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="2ae49-167">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="2ae49-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="2ae49-168">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="2ae49-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="2ae49-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ae49-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="2ae49-170">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="2ae49-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

