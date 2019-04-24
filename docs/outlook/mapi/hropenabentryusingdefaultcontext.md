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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347821"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="d9adc-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="d9adc-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="d9adc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9adc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9adc-105">Realiza a mesma função que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , exceto pelo fato de usar o **emsmdbUID** herdado como o parâmetro _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="d9adc-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="d9adc-106">Não use essa função, a menos que não possa obter o **emsmdbUID** correto para a chamada para [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="d9adc-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9adc-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d9adc-107">Header file:</span></span>  <br/> |<span data-ttu-id="d9adc-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="d9adc-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d9adc-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d9adc-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9adc-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9adc-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d9adc-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d9adc-111">Called by:</span></span>  <br/> |<span data-ttu-id="d9adc-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="d9adc-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d9adc-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9adc-113">Parameters</span></span>

 <span data-ttu-id="d9adc-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d9adc-114">_pmsess_</span></span>
  
> <span data-ttu-id="d9adc-115">no O **IMAPISession**conectado.</span><span class="sxs-lookup"><span data-stu-id="d9adc-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="d9adc-116">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d9adc-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d9adc-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d9adc-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="d9adc-118">no O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d9adc-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d9adc-119">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d9adc-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d9adc-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9adc-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="d9adc-121">no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d9adc-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d9adc-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9adc-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="d9adc-123">no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="d9adc-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="d9adc-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d9adc-124">_lpInterface_</span></span>
  
> <span data-ttu-id="d9adc-125">no Um ponteiro para o identificador de interface (IID) da interface que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="d9adc-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="d9adc-126">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="d9adc-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="d9adc-127">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d9adc-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="d9adc-128">Para listas de distribuição, é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d9adc-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="d9adc-129">Os chamadores podem definir _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="d9adc-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="d9adc-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9adc-130">_ulFlags_</span></span>
  
> <span data-ttu-id="d9adc-131">no Uma bitmask de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="d9adc-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="d9adc-132">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d9adc-132">The following flags can be set:</span></span>
    
<span data-ttu-id="d9adc-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d9adc-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="d9adc-134">Solicita que a entrada seja aberta com o máximo permitido de rede e permissões de cliente.</span><span class="sxs-lookup"><span data-stu-id="d9adc-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="d9adc-135">Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor de catálogo de endereços tentará abrir a entrada com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="d9adc-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="d9adc-136">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="d9adc-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="d9adc-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d9adc-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d9adc-138">Usa apenas o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="d9adc-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d9adc-139">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="d9adc-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d9adc-140">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d9adc-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="d9adc-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d9adc-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="d9adc-142">Permite que a chamada seja bem-sucedida, possivelmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="d9adc-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="d9adc-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d9adc-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="d9adc-144">Usa somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="d9adc-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="d9adc-145">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d9adc-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="d9adc-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d9adc-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="d9adc-147">Solicita que a entrada seja aberta com permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="d9adc-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="d9adc-148">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem supor que a permissão de leitura e gravação tenha sido concedida independentemente de o MAPI_MODIFY ser definido.</span><span class="sxs-lookup"><span data-stu-id="d9adc-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="d9adc-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d9adc-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d9adc-150">Não usa o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="d9adc-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="d9adc-151">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d9adc-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="d9adc-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d9adc-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="d9adc-153">bota Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="d9adc-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="d9adc-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="d9adc-154">_lppUnk_</span></span>
  
> <span data-ttu-id="d9adc-155">bota Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="d9adc-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

