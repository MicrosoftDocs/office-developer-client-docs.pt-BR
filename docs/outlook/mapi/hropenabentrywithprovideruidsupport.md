---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586008"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="b765a-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="b765a-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="b765a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b765a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b765a-105">Realiza a mesma função que a função [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , exceto que a função **HrOpenABEntryWithProviderUIDSupport** abre a entrada usando o objeto de suporte específico em vez de usar a sessão e o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b765a-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b765a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b765a-106">Header file:</span></span>  <br/> |<span data-ttu-id="b765a-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="b765a-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="b765a-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b765a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b765a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b765a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b765a-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b765a-110">Called by:</span></span>  <br/> |<span data-ttu-id="b765a-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b765a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="b765a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b765a-112">Parameters</span></span>

 <span data-ttu-id="b765a-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="b765a-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="b765a-114">[in] Um ponteiro para um parâmetro _emsabpUID_ que identifica o provedor de catálogo de endereços do Exchange que esta função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b765a-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="b765a-115">Se o identificador de entrada de entrada não é um identificador de entrada do Exchange endereço livro provedor, esse parâmetro será ignorado e a age de chamada de função exatamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="b765a-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="b765a-116">Se esse parâmetro for NULL ou um zero MAPIUID, essa função também funciona exatamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="b765a-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="b765a-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="b765a-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="b765a-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b765a-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="b765a-119">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b765a-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b765a-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b765a-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="b765a-121">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="b765a-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="b765a-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b765a-122">_lpInterface_</span></span>
  
> <span data-ttu-id="b765a-123">[in] Um ponteiro para o identificador de interface (IID) da interface a ser usada para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="b765a-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="b765a-124">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="b765a-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="b765a-125">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b765a-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="b765a-126">Para listas de distribuição, ela é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b765a-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="b765a-127">Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="b765a-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="b765a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b765a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b765a-129">[in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="b765a-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="b765a-130">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b765a-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="b765a-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b765a-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="b765a-132">Indica que detalhes retorna TRUE se as alterações são feitas na verdade, o endereço; Caso contrário, detalhes retorna FALSE.</span><span class="sxs-lookup"><span data-stu-id="b765a-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="b765a-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b765a-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="b765a-134">Exibe a versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="b765a-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="b765a-135">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="b765a-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="b765a-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="b765a-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="b765a-137">Exibe a versão sem janela restrita da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="b765a-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="b765a-138">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="b765a-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="b765a-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b765a-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="b765a-140">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b765a-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b765a-141">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b765a-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b765a-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b765a-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="b765a-143">[out] Um ponteiro para o tipo da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="b765a-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="b765a-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b765a-144">_lppUnk_</span></span>
  
> <span data-ttu-id="b765a-145">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="b765a-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

