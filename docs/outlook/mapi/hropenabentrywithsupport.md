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
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766821"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="50b25-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="50b25-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="50b25-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50b25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50b25-105">Não use essa função.</span><span class="sxs-lookup"><span data-stu-id="50b25-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50b25-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="50b25-106">Header file:</span></span>  <br/> |<span data-ttu-id="50b25-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="50b25-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="50b25-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="50b25-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="50b25-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="50b25-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="50b25-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="50b25-110">Called by:</span></span>  <br/> |<span data-ttu-id="50b25-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="50b25-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="50b25-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50b25-112">Parameters</span></span>

 <span data-ttu-id="50b25-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="50b25-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="50b25-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="50b25-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="50b25-115">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="50b25-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="50b25-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="50b25-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="50b25-117">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="50b25-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="50b25-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="50b25-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="50b25-119">[in] Um ponteiro para o identificador de interface (IID) da interface a ser usada para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="50b25-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="50b25-120">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="50b25-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="50b25-121">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="50b25-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="50b25-122">Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md), e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="50b25-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="50b25-123">Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="50b25-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="50b25-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50b25-124">_ulFlags_</span></span>
  
> <span data-ttu-id="50b25-125">[in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="50b25-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="50b25-126">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="50b25-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="50b25-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="50b25-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="50b25-128">Indica que detalhes retorna TRUE se as alterações são feitas na verdade, o endereço; Caso contrário, detalhes retorna FALSE.</span><span class="sxs-lookup"><span data-stu-id="50b25-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="50b25-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="50b25-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="50b25-130">Exibe a versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="50b25-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="50b25-131">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="50b25-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="50b25-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="50b25-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="50b25-133">Exibe a versão sem janela restrita da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="50b25-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="50b25-134">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="50b25-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="50b25-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50b25-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="50b25-136">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="50b25-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="50b25-137">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="50b25-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="50b25-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="50b25-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="50b25-139">[out] Um ponteiro para o tipo da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="50b25-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="50b25-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="50b25-140">_lppUnk_</span></span>
  
> <span data-ttu-id="50b25-141">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="50b25-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

