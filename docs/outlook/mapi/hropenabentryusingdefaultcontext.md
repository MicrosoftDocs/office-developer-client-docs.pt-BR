---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434337"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="01aba-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="01aba-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="01aba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01aba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01aba-105">Executa a mesma função que [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) exceto que ele usa **o emsmdbUID** herdável como o parâmetro _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="01aba-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="01aba-106">Não use essa função, a menos que você não possa obter o **emsmdbUID** correto para a chamada para [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="01aba-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01aba-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="01aba-107">Header file:</span></span>  <br/> |<span data-ttu-id="01aba-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="01aba-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="01aba-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="01aba-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="01aba-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="01aba-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="01aba-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="01aba-111">Called by:</span></span>  <br/> |<span data-ttu-id="01aba-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="01aba-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="01aba-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01aba-113">Parameters</span></span>

 <span data-ttu-id="01aba-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="01aba-114">_pmsess_</span></span>
  
> <span data-ttu-id="01aba-115">[in] O **IMAPISession conectado.**</span><span class="sxs-lookup"><span data-stu-id="01aba-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="01aba-116">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="01aba-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="01aba-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="01aba-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="01aba-118">[in] O livro de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="01aba-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="01aba-119">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="01aba-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="01aba-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="01aba-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="01aba-121">[in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="01aba-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="01aba-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="01aba-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="01aba-123">[in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="01aba-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="01aba-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="01aba-124">_lpInterface_</span></span>
  
> <span data-ttu-id="01aba-125">[in] Um ponteiro para o IID (identificador de interface) da interface que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="01aba-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="01aba-126">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="01aba-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="01aba-127">Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="01aba-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="01aba-128">Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="01aba-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="01aba-129">Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="01aba-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="01aba-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01aba-130">_ulFlags_</span></span>
  
> <span data-ttu-id="01aba-131">[in] Uma máscara de bits de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="01aba-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="01aba-132">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="01aba-132">The following flags can be set:</span></span>
    
<span data-ttu-id="01aba-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="01aba-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="01aba-134">Solicita que a entrada seja aberta com as permissões máximas de rede e cliente permitidas.</span><span class="sxs-lookup"><span data-stu-id="01aba-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="01aba-135">Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor do address book tentará abrir a entrada com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="01aba-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="01aba-136">O cliente pode recuperar o nível de acesso concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="01aba-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="01aba-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="01aba-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="01aba-138">Usa apenas o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="01aba-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="01aba-139">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="01aba-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="01aba-140">Esse sinalizador é suportado apenas pelo provedor de agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="01aba-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="01aba-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="01aba-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="01aba-142">Permite que a chamada seja bem-sucedida, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="01aba-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="01aba-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="01aba-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="01aba-144">Usa somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="01aba-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="01aba-145">Esse sinalizador é suportado apenas pelo provedor de agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="01aba-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="01aba-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="01aba-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="01aba-147">Solicita que a entrada seja aberta com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="01aba-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="01aba-148">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que a permissão de leitura e gravação foi concedida independentemente de MAPI_MODIFY está definida.</span><span class="sxs-lookup"><span data-stu-id="01aba-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="01aba-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="01aba-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="01aba-150">Não usa o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="01aba-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="01aba-151">Esse sinalizador é suportado apenas pelo provedor de agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="01aba-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="01aba-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="01aba-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="01aba-153">[out] Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="01aba-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="01aba-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="01aba-154">_lppUnk_</span></span>
  
> <span data-ttu-id="01aba-155">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="01aba-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

