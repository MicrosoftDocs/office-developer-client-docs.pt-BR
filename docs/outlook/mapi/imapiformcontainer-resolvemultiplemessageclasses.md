---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767026"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="023da-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="023da-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="023da-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="023da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="023da-105">Resolve um grupo de classes de mensagens para seus formulários em um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="023da-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="023da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="023da-106">Parameters</span></span>

 <span data-ttu-id="023da-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="023da-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="023da-108">[in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem para resolver.</span><span class="sxs-lookup"><span data-stu-id="023da-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="023da-109">Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="023da-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="023da-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="023da-110">_ulFlags_</span></span>
  
> <span data-ttu-id="023da-111">[in] Uma bitmask dos sinalizadores que controla como as classes de mensagens forem resolvidas.</span><span class="sxs-lookup"><span data-stu-id="023da-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="023da-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="023da-112">The following flag can be set:</span></span>
    
<span data-ttu-id="023da-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="023da-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="023da-114">Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="023da-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="023da-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="023da-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="023da-116">[out] Um ponteiro para um ponteiro para uma matriz de objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="023da-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="023da-117">Se um aplicativo cliente transmite NULL no parâmetro _pMsgClassArray_ , o parâmetro _ppfrminfoarray_ contém objetos de informações de formulário para todos os formulários no contêiner.</span><span class="sxs-lookup"><span data-stu-id="023da-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="023da-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="023da-118">Return value</span></span>

<span data-ttu-id="023da-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="023da-119">S_OK</span></span> 
  
> <span data-ttu-id="023da-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="023da-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="023da-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="023da-121">Remarks</span></span>

<span data-ttu-id="023da-122">Aplicativos cliente chamam o método de **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="023da-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="023da-123">A matriz de objetos de informações de formulário retornado no parâmetro _ppfrminfoarray_ fornece mais acesso a cada uma das propriedades formas a.</span><span class="sxs-lookup"><span data-stu-id="023da-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="023da-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="023da-124">Notes to callers</span></span>

<span data-ttu-id="023da-125">Para resolver um grupo de classes de mensagens para formulários, passe uma matriz de nomes de classe de mensagem a ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="023da-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="023da-126">Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="023da-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="023da-127">Se uma classe de mensagem não pode ser resolvida para um formulário, NULL é retornada para essa classe de mensagem da matriz de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="023da-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="023da-128">Portanto, mesmo se o método retorna S_OK, não presuma que todas as classes de mensagem foram resolvidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="023da-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="023da-129">Em vez disso, verifique os valores na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="023da-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="023da-130">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="023da-130">MFCMAPI reference</span></span>

<span data-ttu-id="023da-131">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="023da-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="023da-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="023da-132">**File**</span></span>|<span data-ttu-id="023da-133">**Function**</span><span class="sxs-lookup"><span data-stu-id="023da-133">**Function**</span></span>|<span data-ttu-id="023da-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="023da-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="023da-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="023da-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="023da-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="023da-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="023da-137">MFCMAPI usa o método **IMAPIFormContainer::ResolveMultipleMessageClasses** para localizar um formulário que está associado um conjunto de classes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="023da-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="023da-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="023da-138">See also</span></span>



[<span data-ttu-id="023da-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="023da-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="023da-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="023da-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="023da-141">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="023da-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

