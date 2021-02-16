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
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408548"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="be622-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="be622-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="be622-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be622-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be622-105">Resolve uma classe de mensagem para seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.</span><span class="sxs-lookup"><span data-stu-id="be622-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="be622-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be622-106">Parameters</span></span>

 <span data-ttu-id="be622-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="be622-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="be622-108">[in] Uma cadeia de caracteres que nomeia a classe de mensagem que está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="be622-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="be622-109">Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="be622-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="be622-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be622-110">_ulFlags_</span></span>
  
> <span data-ttu-id="be622-111">[in] Uma bitmask de sinalizadores que controla como a classe de mensagem é resolvida.</span><span class="sxs-lookup"><span data-stu-id="be622-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="be622-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="be622-112">The following flag can be set:</span></span>
    
<span data-ttu-id="be622-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="be622-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="be622-114">Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="be622-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="be622-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="be622-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="be622-116">[out] Um ponteiro para um ponteiro para o objeto de informações de formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="be622-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be622-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="be622-117">Return value</span></span>

<span data-ttu-id="be622-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="be622-118">S_OK</span></span> 
  
> <span data-ttu-id="be622-119">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="be622-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="be622-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="be622-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="be622-121">A classe de mensagem passada no  _parâmetro szMessageClass_ não combina com a classe de mensagem de nenhum formulário no contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="be622-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be622-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="be622-122">Remarks</span></span>

<span data-ttu-id="be622-123">Os aplicativos cliente chamam o método **IMAPIFormContainer::ResolveMessageClass** para resolver uma classe de mensagem para um formulário dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="be622-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="be622-124">O objeto de informações de formulário retornado no  _parâmetro ppforminfo_ fornece mais acesso às propriedades do formulário com a classe de mensagem determinada.</span><span class="sxs-lookup"><span data-stu-id="be622-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="be622-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="be622-125">Notes to callers</span></span>

<span data-ttu-id="be622-126">Para resolver uma classe de mensagem para um formulário, passe o nome da classe de mensagem a ser resolvida (por exemplo,  `IPM.HelpDesk.Software` ).</span><span class="sxs-lookup"><span data-stu-id="be622-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="be622-127">Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="be622-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="be622-128">O identificador de classe para a classe de mensagem resolvida é retornado como parte do objeto de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="be622-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="be622-129">Não suponha que o identificador de classe exista na biblioteca OLE até depois de chamar o método [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="be622-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="be622-130">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="be622-130">MFCMAPI reference</span></span>

<span data-ttu-id="be622-131">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="be622-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="be622-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="be622-132">**File**</span></span>|<span data-ttu-id="be622-133">**Função**</span><span class="sxs-lookup"><span data-stu-id="be622-133">**Function**</span></span>|<span data-ttu-id="be622-134">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="be622-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be622-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="be622-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="be622-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="be622-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="be622-137">MFCMAPI usa o **método IMAPIFormContainer::ResolveMessageClass** para localizar um formulário associado a uma classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="be622-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be622-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="be622-138">See also</span></span>



[<span data-ttu-id="be622-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="be622-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="be622-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="be622-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="be622-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="be622-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="be622-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be622-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

