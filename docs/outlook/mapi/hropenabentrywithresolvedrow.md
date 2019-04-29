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
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429905"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="37717-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="37717-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="37717-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37717-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37717-105">Realiza a mesma função que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , exceto pelo fato de que ela obtém automaticamente o **emsabpUID** da linha resolvida e abre a **EntryID**.</span><span class="sxs-lookup"><span data-stu-id="37717-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37717-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="37717-106">Header file:</span></span>  <br/> |<span data-ttu-id="37717-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="37717-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="37717-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="37717-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="37717-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="37717-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="37717-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="37717-110">Called by:</span></span>  <br/> |<span data-ttu-id="37717-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="37717-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="37717-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37717-112">Parameters</span></span>

 <span data-ttu-id="37717-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="37717-113">_prwResolved_</span></span>
  
> <span data-ttu-id="37717-114">no Um ponteiro para a linha resolvida que é usada para obter o **emsabpUID** e abrir a **EntryID**.</span><span class="sxs-lookup"><span data-stu-id="37717-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="37717-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="37717-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="37717-116">no O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="37717-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="37717-117">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="37717-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="37717-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="37717-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="37717-119">no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="37717-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="37717-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="37717-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="37717-121">no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="37717-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="37717-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="37717-122">_lpInterface_</span></span>
  
> <span data-ttu-id="37717-123">no Um ponteiro para o identificador de interface (IID) da interface que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="37717-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="37717-124">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="37717-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="37717-125">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="37717-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="37717-126">Para listas de distribuição, é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêiners, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="37717-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="37717-127">Os chamadores podem definir _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="37717-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="37717-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37717-128">_ulFlags_</span></span>
  
> <span data-ttu-id="37717-129">no Uma bitmask de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="37717-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="37717-130">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="37717-130">The following flags can be set:</span></span>
    
<span data-ttu-id="37717-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="37717-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="37717-132">Solicita que a entrada seja aberta com o máximo permitido de rede e permissões de cliente.</span><span class="sxs-lookup"><span data-stu-id="37717-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="37717-133">Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor de catálogo de endereços tentará abrir a entrada com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="37717-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="37717-134">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="37717-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="37717-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="37717-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="37717-136">Usa apenas o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="37717-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="37717-137">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="37717-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="37717-138">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="37717-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="37717-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="37717-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="37717-140">Permite que a chamada seja bem-sucedida, possivelmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="37717-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="37717-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="37717-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="37717-142">Usa somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="37717-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="37717-143">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="37717-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="37717-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="37717-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="37717-145">Solicita que a entrada seja aberta com permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="37717-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="37717-146">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem supor que a permissão de leitura e gravação tenha sido concedida independentemente de o MAPI_MODIFY ser definido.</span><span class="sxs-lookup"><span data-stu-id="37717-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="37717-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="37717-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="37717-148">Não usa o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="37717-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="37717-149">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="37717-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="37717-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="37717-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="37717-151">bota Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="37717-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="37717-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="37717-152">_lppUnk_</span></span>
  
> <span data-ttu-id="37717-153">bota Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="37717-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

