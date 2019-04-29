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
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426391"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="20565-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="20565-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="20565-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20565-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20565-105">Resolve uma classe de mensagem para seu formulário dentro de um contêiner de formulários e retorna um objeto de informações de formulário para esse formulário.</span><span class="sxs-lookup"><span data-stu-id="20565-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="20565-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20565-106">Parameters</span></span>

 <span data-ttu-id="20565-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="20565-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="20565-108">no Uma cadeia de caracteres que nomeia a classe da mensagem que está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="20565-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="20565-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20565-109">_ulFlags_</span></span>
  
> <span data-ttu-id="20565-110">no Uma bitmask de sinalizadores que controla como a classe da mensagem é resolvida.</span><span class="sxs-lookup"><span data-stu-id="20565-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="20565-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="20565-111">The following flag can be set:</span></span>
    
<span data-ttu-id="20565-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="20565-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="20565-113">Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="20565-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="20565-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="20565-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="20565-115">no Um ponteiro para a pasta que contém a mensagem que está sendo resolvida.</span><span class="sxs-lookup"><span data-stu-id="20565-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="20565-116">O parâmetro _pFolderFocus_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="20565-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="20565-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="20565-117">_ppResult_</span></span>
  
> <span data-ttu-id="20565-118">bota Um ponteiro para um ponteiro para um objeto de informações do formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="20565-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20565-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20565-119">Return value</span></span>

<span data-ttu-id="20565-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="20565-120">S_OK</span></span> 
  
> <span data-ttu-id="20565-121">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="20565-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="20565-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="20565-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="20565-123">A classe de mensagem passada no parâmetro _szMsgClass_ não corresponde à classe de mensagem de nenhum formulário na biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="20565-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="20565-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="20565-124">Remarks</span></span>

<span data-ttu-id="20565-125">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: ResolveMessageClass** para resolver uma classe de mensagem para seu formulário dentro de um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="20565-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="20565-126">O objeto de informações de formulário retornado no parâmetro _ppResult_ fornece acesso adicional às propriedades do formulário que tem a classe de mensagem determinada.</span><span class="sxs-lookup"><span data-stu-id="20565-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="20565-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="20565-127">Notes to callers</span></span>

<span data-ttu-id="20565-128">Para resolver uma classe de mensagem para um formulário, um visualizador de formulários passa o nome da classe de mensagem a ser resolvida, como `IPM.HelpDesk.Software`"".</span><span class="sxs-lookup"><span data-stu-id="20565-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="20565-129">Para forçar a resolução a ser exata (ou seja, para impedir a resolução de uma classe base da classe de mensagem quando um servidor de formulário com correspondência exata não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="20565-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="20565-130">Se o parâmetro _pFolderFocus_ for NULL, o processo de resolução da classe de mensagem não pesquisará um contêiner de pasta.</span><span class="sxs-lookup"><span data-stu-id="20565-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="20565-131">A ordem dos contêineres pesquisada depende da implementação do provedor de biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="20565-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="20565-132">O provedor de biblioteca de formulários padrão pesquisa primeiro o contêiner local e, em seguida, o contêiner de pasta para a pasta passada, o contêiner de formulário pessoal e, por fim, o contêiner da organização.</span><span class="sxs-lookup"><span data-stu-id="20565-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="20565-133">Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="20565-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="20565-134">O identificador de classe da classe de mensagem resolvida é retornado como parte do objeto de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="20565-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="20565-135">Um visualizador de formulários não deve funcionar na pressuposição de que o identificador de classe existe na biblioteca OLE até que o Visualizador de formulários tenha chamado o método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) ou o método [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="20565-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20565-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="20565-136">See also</span></span>



[<span data-ttu-id="20565-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="20565-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="20565-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="20565-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="20565-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="20565-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="20565-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20565-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

