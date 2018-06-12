---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 74660de551d43c589cb903b5c3852136f2f18269
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766799"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="a4b33-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="a4b33-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="a4b33-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4b33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4b33-105">Realiza a mesma função que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , exceto que ele usa o herdado **emsmdbUID** como o parâmetro _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="a4b33-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="a4b33-106">Não use essa função, a menos que você não pode obter o **emsmdbUID** correto para a chamada para [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="a4b33-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4b33-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a4b33-107">Header file:</span></span>  <br/> |<span data-ttu-id="a4b33-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a4b33-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a4b33-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a4b33-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4b33-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4b33-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4b33-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a4b33-111">Called by:</span></span>  <br/> |<span data-ttu-id="a4b33-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a4b33-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a4b33-113">Par�metros</span><span class="sxs-lookup"><span data-stu-id="a4b33-113">Parameters</span></span>

 <span data-ttu-id="a4b33-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="a4b33-114">_pmsess_</span></span>
  
> <span data-ttu-id="a4b33-115">[in] O conectado **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="a4b33-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="a4b33-116">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a4b33-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a4b33-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a4b33-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="a4b33-118">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4b33-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a4b33-119">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a4b33-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a4b33-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a4b33-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="a4b33-121">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a4b33-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a4b33-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a4b33-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="a4b33-123">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="a4b33-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="a4b33-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a4b33-124">_lpInterface_</span></span>
  
> <span data-ttu-id="a4b33-125">[in] Um ponteiro para o identificador de interface (IID) da interface do que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="a4b33-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="a4b33-126">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="a4b33-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a4b33-127">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a4b33-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a4b33-128">Para listas de distribuição, ela é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a4b33-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a4b33-129">Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="a4b33-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a4b33-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4b33-130">_ulFlags_</span></span>
  
> <span data-ttu-id="a4b33-131">[in] Uma bitmask dos sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="a4b33-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="a4b33-132">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a4b33-132">The following flags can be set:</span></span>
    
<span data-ttu-id="a4b33-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a4b33-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="a4b33-134">Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas.</span><span class="sxs-lookup"><span data-stu-id="a4b33-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="a4b33-135">Por exemplo, se o cliente tem de leitura e permissão de gravação, o provedor de catálogo de endereços tenta abrir a entrada com a leitura e a permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="a4b33-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="a4b33-136">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="a4b33-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="a4b33-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="a4b33-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="a4b33-138">Usa apenas o catálogo de endereços offline para realizar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="a4b33-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="a4b33-139">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="a4b33-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="a4b33-140">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4b33-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="a4b33-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a4b33-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="a4b33-142">Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes à entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="a4b33-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="a4b33-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="a4b33-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="a4b33-144">Usa apenas a GAL para realizar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="a4b33-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="a4b33-145">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4b33-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="a4b33-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a4b33-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="a4b33-147">Solicitações que a entrada ser aberto com leia e permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="a4b33-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="a4b33-148">Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que ler e gravar a permissão foi concedida independentemente MAPI_MODIFY é definida.</span><span class="sxs-lookup"><span data-stu-id="a4b33-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="a4b33-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="a4b33-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="a4b33-150">Não usa o catálogo de endereços offline para executar a resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="a4b33-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="a4b33-151">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4b33-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="a4b33-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a4b33-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="a4b33-153">[out] Um ponteiro para o tipo da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="a4b33-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a4b33-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a4b33-154">_lppUnk_</span></span>
  
> <span data-ttu-id="a4b33-155">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="a4b33-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

