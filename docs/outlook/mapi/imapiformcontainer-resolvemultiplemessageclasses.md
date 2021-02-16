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
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412538"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="1a90d-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="1a90d-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="1a90d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a90d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a90d-105">Resolve um grupo de classes de mensagem para seus formulários em um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="1a90d-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="1a90d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a90d-106">Parameters</span></span>

 <span data-ttu-id="1a90d-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="1a90d-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="1a90d-108">[in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem a resolver.</span><span class="sxs-lookup"><span data-stu-id="1a90d-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="1a90d-109">Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="1a90d-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="1a90d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a90d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1a90d-111">[in] Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="1a90d-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="1a90d-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1a90d-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1a90d-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="1a90d-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="1a90d-114">Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="1a90d-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="1a90d-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="1a90d-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="1a90d-116">[out] Um ponteiro para um ponteiro para uma matriz de objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="1a90d-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="1a90d-117">Se um aplicativo cliente passar NULL no parâmetro  _pMsgClassArray,_ o parâmetro  _ppfrminfoarray_ conterá objetos de informações de formulário para todos os formulários no contêiner.</span><span class="sxs-lookup"><span data-stu-id="1a90d-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a90d-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1a90d-118">Return value</span></span>

<span data-ttu-id="1a90d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a90d-119">S_OK</span></span> 
  
> <span data-ttu-id="1a90d-120">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1a90d-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a90d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a90d-121">Remarks</span></span>

<span data-ttu-id="1a90d-122">Os aplicativos cliente chamam o método **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="1a90d-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="1a90d-123">A matriz de objetos de informações de formulário retornados no  _parâmetro ppfrminfoarray_ fornece mais acesso a cada uma das propriedades dos formulários.</span><span class="sxs-lookup"><span data-stu-id="1a90d-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a90d-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1a90d-124">Notes to callers</span></span>

<span data-ttu-id="1a90d-125">Para resolver um grupo de classes de mensagens para formulários, passe uma matriz de nomes de classe de mensagem a serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="1a90d-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="1a90d-126">Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="1a90d-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="1a90d-127">Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="1a90d-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="1a90d-128">Portanto, mesmo que o método retorne S_OK, não suponha que todas as classes de mensagens foram resolvidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="1a90d-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="1a90d-129">Em vez disso, verifique os valores na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="1a90d-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1a90d-130">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1a90d-130">MFCMAPI reference</span></span>

<span data-ttu-id="1a90d-131">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a90d-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1a90d-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1a90d-132">**File**</span></span>|<span data-ttu-id="1a90d-133">**Função**</span><span class="sxs-lookup"><span data-stu-id="1a90d-133">**Function**</span></span>|<span data-ttu-id="1a90d-134">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1a90d-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a90d-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1a90d-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="1a90d-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="1a90d-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="1a90d-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span><span class="sxs-lookup"><span data-stu-id="1a90d-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a90d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a90d-138">See also</span></span>



[<span data-ttu-id="1a90d-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="1a90d-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="1a90d-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a90d-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="1a90d-141">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1a90d-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

