---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767021"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="df68c-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="df68c-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="df68c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df68c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df68c-105">Resolve uma classe de mensagem para o seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="df68c-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="df68c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df68c-106">Parameters</span></span>

 <span data-ttu-id="df68c-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="df68c-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="df68c-108">[in] Uma cadeia de caracteres que nomeia a classe de mensagem que está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="df68c-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="df68c-109">Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="df68c-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="df68c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df68c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="df68c-111">[in] Uma bitmask dos sinalizadores que controla como a classe da mensagem for resolvida.</span><span class="sxs-lookup"><span data-stu-id="df68c-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="df68c-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="df68c-112">The following flag can be set:</span></span>
    
<span data-ttu-id="df68c-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="df68c-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="df68c-114">Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="df68c-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="df68c-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="df68c-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="df68c-116">[out] Um ponteiro para um ponteiro para o objeto de informações do formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="df68c-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df68c-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="df68c-117">Return value</span></span>

<span data-ttu-id="df68c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="df68c-118">S_OK</span></span> 
  
> <span data-ttu-id="df68c-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="df68c-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="df68c-120">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="df68c-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="df68c-121">A classe de mensagem passada no parâmetro _szMessageClass_ não coincide com a classe de mensagem para qualquer formulário no contêiner do formulário.</span><span class="sxs-lookup"><span data-stu-id="df68c-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df68c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="df68c-122">Remarks</span></span>

<span data-ttu-id="df68c-123">Aplicativos cliente chamam o método de **IMAPIFormContainer::ResolveMessageClass** para resolver uma classe de mensagem para um formulário dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="df68c-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="df68c-124">O objeto de informações do formulário retornado no parâmetro _ppforminfo_ fornece mais acesso às propriedades do formulário com a classe de mensagem determinado.</span><span class="sxs-lookup"><span data-stu-id="df68c-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="df68c-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="df68c-125">Notes to callers</span></span>

<span data-ttu-id="df68c-126">Para resolver uma classe de mensagem para um formulário, passar o nome de classe de mensagem a ser resolvido (por exemplo, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="df68c-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="df68c-127">Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="df68c-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="df68c-128">O identificador de classe para a classe de mensagem resolvido é retornado como parte do objeto de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="df68c-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="df68c-129">Não presuma que o identificador de classe existe na biblioteca do OLE até depois que você chama o método o [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="df68c-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="df68c-130">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="df68c-130">MFCMAPI reference</span></span>

<span data-ttu-id="df68c-131">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="df68c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="df68c-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="df68c-132">**File**</span></span>|<span data-ttu-id="df68c-133">**Function**</span><span class="sxs-lookup"><span data-stu-id="df68c-133">**Function**</span></span>|<span data-ttu-id="df68c-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="df68c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="df68c-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="df68c-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="df68c-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="df68c-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="df68c-137">MFCMAPI usa o método **IMAPIFormContainer::ResolveMessageClass** para localizar um formulário que está associado uma classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="df68c-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df68c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="df68c-138">See also</span></span>



[<span data-ttu-id="df68c-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="df68c-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="df68c-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="df68c-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="df68c-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="df68c-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="df68c-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df68c-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

