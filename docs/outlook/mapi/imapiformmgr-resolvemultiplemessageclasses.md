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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad2014d1d003a4d80646ed1b679f0d3827341c1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767050"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="121fd-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="121fd-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="121fd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="121fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="121fd-105">Resolve um grupo de classes de mensagens para seus formulários dentro de um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="121fd-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="121fd-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="121fd-106">Parameters</span></span>

 <span data-ttu-id="121fd-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="121fd-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="121fd-108">[in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem para resolver.</span><span class="sxs-lookup"><span data-stu-id="121fd-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="121fd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="121fd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="121fd-110">[in] Uma bitmask dos sinalizadores que controla como as classes de mensagens forem resolvidas.</span><span class="sxs-lookup"><span data-stu-id="121fd-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="121fd-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="121fd-111">The following flag can be set:</span></span>
    
<span data-ttu-id="121fd-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="121fd-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="121fd-113">Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="121fd-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="121fd-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="121fd-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="121fd-115">Não inclua formulários armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="121fd-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="121fd-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="121fd-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="121fd-117">[in] Um ponteiro para a pasta que contém o formulário cujo classe de mensagem está sendo resolvido.</span><span class="sxs-lookup"><span data-stu-id="121fd-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="121fd-118">O parâmetro _pFolderFocus_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="121fd-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="121fd-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="121fd-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="121fd-120">[out] Um ponteiro para um ponteiro para uma matriz de objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="121fd-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="121fd-121">Se um visualizador de formulário transmite NULL no parâmetro _pMsgClasses_ , o parâmetro _ppfrminfoarray_ contém objetos de informações de formulário para todos os formulários no contêiner.</span><span class="sxs-lookup"><span data-stu-id="121fd-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="121fd-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="121fd-122">Return value</span></span>

<span data-ttu-id="121fd-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="121fd-123">S_OK</span></span> 
  
> <span data-ttu-id="121fd-124">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="121fd-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="121fd-125">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="121fd-125">Remarks</span></span>

<span data-ttu-id="121fd-126">Visualizadores de formulário chame o método de **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="121fd-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="121fd-127">A matriz de objetos do formulário informações retornadas nos _ppfrminfoarray_ fornece mais acesso a cada uma das propriedades formas a.</span><span class="sxs-lookup"><span data-stu-id="121fd-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="121fd-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="121fd-128">Notes to callers</span></span>

<span data-ttu-id="121fd-129">Para resolver um grupo de classes de mensagens para formulários, um visualizador de formulário passa em uma matriz de nomes de classe de mensagem a ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="121fd-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="121fd-130">Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um formulário exatamente correspondente servidor não está disponível) o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="121fd-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="121fd-131">Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="121fd-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="121fd-132">Se uma classe de mensagem não pode ser resolvida para um formulário, NULL é retornada para essa classe de mensagem da matriz de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="121fd-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="121fd-133">Portanto, mesmo se o método retorna S_OK, visualizadores do formulário não devem funcionar no pressuposto de que todas as classes de mensagem foram resolvidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="121fd-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="121fd-134">Em vez disso, os visualizadores de formulário devem verificar os valores na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="121fd-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="121fd-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="121fd-135">See also</span></span>



[<span data-ttu-id="121fd-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="121fd-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="121fd-137">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="121fd-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

