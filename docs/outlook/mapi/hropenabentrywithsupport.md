---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 58a6249295810e32c0a0f845e4830b8f393885ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579379"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="18626-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="18626-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="18626-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18626-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18626-105">Não use essa função.</span><span class="sxs-lookup"><span data-stu-id="18626-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18626-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="18626-106">Header file:</span></span>  <br/> |<span data-ttu-id="18626-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="18626-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="18626-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="18626-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="18626-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="18626-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="18626-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="18626-110">Called by:</span></span>  <br/> |<span data-ttu-id="18626-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="18626-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="18626-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18626-112">Parameters</span></span>

 <span data-ttu-id="18626-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="18626-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="18626-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="18626-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="18626-115">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="18626-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="18626-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="18626-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="18626-117">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="18626-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="18626-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="18626-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="18626-119">[in] Um ponteiro para o identificador de interface (IID) da interface a ser usada para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="18626-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="18626-120">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="18626-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="18626-121">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="18626-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="18626-122">Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md), e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="18626-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="18626-123">Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="18626-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="18626-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18626-124">_ulFlags_</span></span>
  
> <span data-ttu-id="18626-125">[in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="18626-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="18626-126">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="18626-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="18626-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="18626-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="18626-128">Indica que detalhes retorna TRUE se as alterações são feitas na verdade, o endereço; Caso contrário, detalhes retorna FALSE.</span><span class="sxs-lookup"><span data-stu-id="18626-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="18626-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="18626-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="18626-130">Exibe a versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="18626-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="18626-131">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="18626-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="18626-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="18626-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="18626-133">Exibe a versão sem janela restrita da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="18626-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="18626-134">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="18626-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="18626-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="18626-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="18626-136">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="18626-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="18626-137">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="18626-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="18626-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="18626-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="18626-139">[out] Um ponteiro para o tipo da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="18626-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="18626-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="18626-140">_lppUnk_</span></span>
  
> <span data-ttu-id="18626-141">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="18626-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

