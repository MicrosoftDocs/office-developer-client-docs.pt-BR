---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3cd84e4ddb6d722d9f3de11d65b100d86e69ecae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571812"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="2456e-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="2456e-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="2456e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2456e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2456e-105">Resolve uma classe de mensagem para o seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="2456e-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="2456e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2456e-106">Parameters</span></span>

 <span data-ttu-id="2456e-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="2456e-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="2456e-108">[in] Uma cadeia de caracteres que nomeia a classe de mensagem que está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="2456e-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="2456e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2456e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2456e-110">[in] Uma bitmask dos sinalizadores que controla como a classe da mensagem for resolvida.</span><span class="sxs-lookup"><span data-stu-id="2456e-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="2456e-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="2456e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2456e-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="2456e-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="2456e-113">Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="2456e-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="2456e-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="2456e-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="2456e-115">[in] Um ponteiro para a pasta que contém a mensagem que está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="2456e-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="2456e-116">O parâmetro _pFolderFocus_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2456e-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="2456e-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="2456e-117">_ppResult_</span></span>
  
> <span data-ttu-id="2456e-118">[out] Um ponteiro para um ponteiro para um objeto de informações do formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="2456e-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2456e-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2456e-119">Return value</span></span>

<span data-ttu-id="2456e-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="2456e-120">S_OK</span></span> 
  
> <span data-ttu-id="2456e-121">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="2456e-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2456e-122">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2456e-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2456e-123">A classe de mensagem passada no parâmetro _szMsgClass_ não coincide com a classe de mensagem para qualquer formulário na biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="2456e-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2456e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2456e-124">Remarks</span></span>

<span data-ttu-id="2456e-125">Visualizadores de formulário chame o método de **IMAPIFormMgr::ResolveMessageClass** para resolver uma classe de mensagem para o seu formulário dentro de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="2456e-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="2456e-126">O objeto de informações do formulário retornado no parâmetro _ppResult_ fornece mais acesso às propriedades do formulário que tem a classe de mensagem determinado.</span><span class="sxs-lookup"><span data-stu-id="2456e-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2456e-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="2456e-127">Notes to callers</span></span>

<span data-ttu-id="2456e-128">Para resolver uma classe de mensagem para um formulário, um visualizador de formulário passa no nome de classe de mensagem ser resolvidos, como " `IPM.HelpDesk.Software`".</span><span class="sxs-lookup"><span data-stu-id="2456e-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="2456e-129">Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um formulário exatamente correspondente server não está disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2456e-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="2456e-130">Se o parâmetro _pFolderFocus_ for NULL, o processo de resolução de classe de mensagem não procura um contêiner de pasta.</span><span class="sxs-lookup"><span data-stu-id="2456e-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="2456e-131">A ordem dos contêineres pesquisadas depende a implementação do provedor de biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="2456e-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="2456e-132">O provedor de biblioteca de formulário padrão pesquisa primeiro o contêiner de local, em seguida, o contêiner de pasta para a pasta de no passado, o contêiner de formulários particular e, por fim, o contêiner da organização.</span><span class="sxs-lookup"><span data-stu-id="2456e-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="2456e-133">Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="2456e-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="2456e-134">O identificador de classe para a classe de mensagem resolvido é retornado como parte do objeto de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="2456e-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="2456e-135">Um visualizador de formulário não deve funcionar no pressuposto de que o identificador de classe existe na biblioteca do OLE até depois que a tela de formulário tiver chamado o método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou o método [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="2456e-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2456e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2456e-136">See also</span></span>



[<span data-ttu-id="2456e-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2456e-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="2456e-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="2456e-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="2456e-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="2456e-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="2456e-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2456e-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

