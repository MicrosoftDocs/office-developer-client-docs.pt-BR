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
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417641"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="e6802-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="e6802-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="e6802-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6802-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6802-105">Não use essa função.</span><span class="sxs-lookup"><span data-stu-id="e6802-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6802-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e6802-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6802-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e6802-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e6802-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e6802-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6802-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6802-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e6802-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e6802-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6802-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="e6802-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e6802-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6802-112">Parameters</span></span>

 <span data-ttu-id="e6802-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="e6802-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="e6802-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e6802-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="e6802-115">[in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="e6802-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e6802-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e6802-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="e6802-117">[in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="e6802-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="e6802-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e6802-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="e6802-119">[in] Um ponteiro para o IID (identificador de interface) da interface a ser usada para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="e6802-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="e6802-120">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6802-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="e6802-121">Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="e6802-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="e6802-122">Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e6802-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="e6802-123">Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="e6802-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="e6802-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6802-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e6802-125">[in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="e6802-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="e6802-126">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e6802-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="e6802-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="e6802-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="e6802-128">Indica que Details retornará TRUE se as alterações realmente foram feitas no endereço; Caso contrário, Details retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="e6802-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="e6802-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="e6802-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="e6802-130">Exibe a versão modal da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="e6802-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="e6802-131">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="e6802-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="e6802-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="e6802-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="e6802-133">Exibe a versão sem modo da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="e6802-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="e6802-134">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="e6802-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="e6802-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6802-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="e6802-136">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e6802-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e6802-137">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e6802-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e6802-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="e6802-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="e6802-139">[out] Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="e6802-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="e6802-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="e6802-140">_lppUnk_</span></span>
  
> <span data-ttu-id="e6802-141">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="e6802-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

