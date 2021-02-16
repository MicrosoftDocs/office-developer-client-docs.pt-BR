---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428015"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="960cc-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="960cc-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="960cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="960cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="960cc-105">Resolve um grupo de classes de mensagem para seus formulários dentro de um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="960cc-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="960cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="960cc-106">Parameters</span></span>

 <span data-ttu-id="960cc-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="960cc-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="960cc-108">[in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem a resolver.</span><span class="sxs-lookup"><span data-stu-id="960cc-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="960cc-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="960cc-109">_ulFlags_</span></span>
  
> <span data-ttu-id="960cc-110">[in] Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="960cc-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="960cc-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="960cc-111">The following flag can be set:</span></span>
    
<span data-ttu-id="960cc-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="960cc-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="960cc-113">Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="960cc-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="960cc-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="960cc-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="960cc-115">Não inclua formulários armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="960cc-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="960cc-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="960cc-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="960cc-117">[in] Um ponteiro para a pasta que contém o formulário cuja classe de mensagem está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="960cc-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="960cc-118">O  _parâmetro pFolderFocus_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="960cc-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="960cc-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="960cc-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="960cc-120">[out] Um ponteiro para um ponteiro para uma matriz de objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="960cc-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="960cc-121">Se um visualizador de formulários passar NULL no parâmetro  _pMsgClasses,_ o parâmetro  _ppfrminfoarray_ conterá objetos de informações de formulário para todos os formulários no contêiner.</span><span class="sxs-lookup"><span data-stu-id="960cc-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="960cc-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="960cc-122">Return value</span></span>

<span data-ttu-id="960cc-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="960cc-123">S_OK</span></span> 
  
> <span data-ttu-id="960cc-124">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="960cc-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="960cc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="960cc-125">Remarks</span></span>

<span data-ttu-id="960cc-126">Visualizadores de formulário chamam o método **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="960cc-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="960cc-127">A matriz de objetos de informações de formulário  _retornados em ppfrminfoarray_ fornece mais acesso a cada uma das propriedades dos formulários.</span><span class="sxs-lookup"><span data-stu-id="960cc-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="960cc-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="960cc-128">Notes to callers</span></span>

<span data-ttu-id="960cc-129">Para resolver um grupo de classes de mensagens para formulários, um visualizador de formulários passa uma matriz de nomes de classe de mensagem a serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="960cc-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="960cc-130">Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um servidor de formulário exatamente correspondente não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="960cc-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="960cc-131">Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="960cc-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="960cc-132">Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="960cc-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="960cc-133">Portanto, mesmo que o método retorne S_OK, os visualizadores de formulário não devem trabalhar com a suposição de que todas as classes de mensagens foram resolvidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="960cc-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="960cc-134">Em vez disso, os visualizadores de formulário devem verificar os valores na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="960cc-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="960cc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="960cc-135">See also</span></span>



[<span data-ttu-id="960cc-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="960cc-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="960cc-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="960cc-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

