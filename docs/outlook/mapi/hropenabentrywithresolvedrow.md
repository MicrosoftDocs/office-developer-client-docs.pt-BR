---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9572f44f1f4865fcce5d7aa8bd8478340b0de968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594716"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="6f137-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="6f137-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="6f137-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f137-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f137-105">Realiza a mesma função que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , exceto que ele obtém o **emsabpUID** da linha resolvida automaticamente e abre a **entryID**.</span><span class="sxs-lookup"><span data-stu-id="6f137-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f137-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6f137-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f137-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="6f137-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="6f137-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="6f137-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6f137-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6f137-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6f137-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="6f137-110">Called by:</span></span>  <br/> |<span data-ttu-id="6f137-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="6f137-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="6f137-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f137-112">Parameters</span></span>

 <span data-ttu-id="6f137-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="6f137-113">_prwResolved_</span></span>
  
> <span data-ttu-id="6f137-114">[in] Um ponteiro para a linha resolvido que é usado para fazer o **emsabpUID** e abra a **entryID**.</span><span class="sxs-lookup"><span data-stu-id="6f137-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="6f137-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="6f137-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="6f137-116">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f137-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="6f137-117">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="6f137-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="6f137-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6f137-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="6f137-119">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="6f137-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6f137-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6f137-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="6f137-121">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="6f137-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="6f137-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6f137-122">_lpInterface_</span></span>
  
> <span data-ttu-id="6f137-123">[in] Um ponteiro para o identificador de interface (IID) da interface do que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="6f137-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="6f137-124">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="6f137-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="6f137-125">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6f137-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="6f137-126">Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="6f137-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="6f137-127">Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="6f137-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="6f137-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f137-128">_ulFlags_</span></span>
  
> <span data-ttu-id="6f137-129">[in] Uma bitmask dos sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="6f137-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="6f137-130">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6f137-130">The following flags can be set:</span></span>
    
<span data-ttu-id="6f137-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6f137-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="6f137-132">Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas.</span><span class="sxs-lookup"><span data-stu-id="6f137-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="6f137-133">Por exemplo, se o cliente tem de leitura e permissão de gravação, o provedor de catálogo de endereços tenta abrir a entrada com a leitura e a permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="6f137-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="6f137-134">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="6f137-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="6f137-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="6f137-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="6f137-136">Usa apenas o catálogo de endereços offline para realizar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="6f137-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="6f137-137">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="6f137-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="6f137-138">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f137-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6f137-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6f137-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="6f137-140">Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes à entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="6f137-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="6f137-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="6f137-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="6f137-142">Usa apenas a GAL para realizar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="6f137-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="6f137-143">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f137-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6f137-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6f137-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="6f137-145">Solicitações que a entrada ser aberto com leia e permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="6f137-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="6f137-146">Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que ler e gravar a permissão foi concedida independentemente MAPI_MODIFY é definida.</span><span class="sxs-lookup"><span data-stu-id="6f137-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="6f137-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="6f137-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="6f137-148">Não usa o catálogo de endereços offline para executar a resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="6f137-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="6f137-149">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f137-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="6f137-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6f137-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="6f137-151">[out] Um ponteiro para o tipo da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="6f137-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="6f137-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="6f137-152">_lppUnk_</span></span>
  
> <span data-ttu-id="6f137-153">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="6f137-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

