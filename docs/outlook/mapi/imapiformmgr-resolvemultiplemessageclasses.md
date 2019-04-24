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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321865"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="3be62-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="3be62-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="3be62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3be62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3be62-105">Resolve um grupo de classes de mensagem para seus formulários dentro de um contêiner de formulários e retorna uma matriz de objetos de informações de formulário para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="3be62-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="3be62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3be62-106">Parameters</span></span>

 <span data-ttu-id="3be62-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="3be62-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="3be62-108">no Um ponteiro para uma matriz que contém os nomes das classes de mensagens a serem resolvidas.</span><span class="sxs-lookup"><span data-stu-id="3be62-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="3be62-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3be62-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3be62-110">no Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="3be62-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="3be62-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3be62-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3be62-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="3be62-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="3be62-113">Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="3be62-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="3be62-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="3be62-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="3be62-115">Não inclua formulários armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="3be62-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="3be62-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="3be62-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="3be62-117">no Um ponteiro para a pasta que contém o formulário cuja classe de mensagem está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="3be62-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="3be62-118">O parâmetro _pFolderFocus_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="3be62-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="3be62-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="3be62-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="3be62-120">bota Um ponteiro para um ponteiro para uma matriz de objetos de informação do formulário.</span><span class="sxs-lookup"><span data-stu-id="3be62-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="3be62-121">Se um visualizador de formulários passar nulo no parâmetro _pMsgClasses_ , o parâmetro _ppfrminfoarray_ contém objetos de informações de formulário para todos os formulários no contêiner.</span><span class="sxs-lookup"><span data-stu-id="3be62-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3be62-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3be62-122">Return value</span></span>

<span data-ttu-id="3be62-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="3be62-123">S_OK</span></span> 
  
> <span data-ttu-id="3be62-124">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3be62-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3be62-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3be62-125">Remarks</span></span>

<span data-ttu-id="3be62-126">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagem para formulários dentro de um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="3be62-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="3be62-127">A matriz de objetos de informações de formulário retornada no _ppfrminfoarray_ fornece acesso adicional a cada uma das propriedades de formulários.</span><span class="sxs-lookup"><span data-stu-id="3be62-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3be62-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3be62-128">Notes to callers</span></span>

<span data-ttu-id="3be62-129">Para resolver um grupo de classes de mensagem para formulários, um visualizador de formulários passa em uma matriz de nomes de classe de mensagem a ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="3be62-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="3be62-130">Para forçar a resolução a ser exata (ou seja, para impedir a resolução de uma classe base da classe de mensagem quando um servidor de formulário com correspondência exata não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="3be62-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="3be62-131">Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="3be62-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="3be62-132">Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="3be62-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="3be62-133">Portanto, mesmo que o método retorne S_OK, os visualizadores de formulário não devem funcionar na pressuposição de que todas as classes de mensagens tenham sido resolvidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="3be62-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="3be62-134">Em vez disso, os visualizadores de formulário devem verificar os valores na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="3be62-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3be62-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3be62-135">See also</span></span>



[<span data-ttu-id="3be62-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="3be62-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="3be62-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3be62-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

