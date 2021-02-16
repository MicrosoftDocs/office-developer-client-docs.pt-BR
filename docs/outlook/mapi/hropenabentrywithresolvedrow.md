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
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="eda42-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="eda42-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="eda42-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eda42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eda42-105">Executa a mesma função que [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) exceto que ele obtém automaticamente **o emsabpUID** da linha resolvida e abre a **entryID**.</span><span class="sxs-lookup"><span data-stu-id="eda42-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eda42-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eda42-106">Header file:</span></span>  <br/> |<span data-ttu-id="eda42-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="eda42-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="eda42-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eda42-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eda42-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eda42-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eda42-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="eda42-110">Called by:</span></span>  <br/> |<span data-ttu-id="eda42-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="eda42-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="eda42-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eda42-112">Parameters</span></span>

 <span data-ttu-id="eda42-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="eda42-113">_prwResolved_</span></span>
  
> <span data-ttu-id="eda42-114">[in] Um ponteiro para a linha resolvida que é usada para obter o **emsabpUID** e abrir a **entryID**.</span><span class="sxs-lookup"><span data-stu-id="eda42-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="eda42-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="eda42-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="eda42-116">[in] O livro de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="eda42-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="eda42-117">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="eda42-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="eda42-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="eda42-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="eda42-119">[in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="eda42-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="eda42-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="eda42-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="eda42-121">[in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="eda42-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="eda42-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="eda42-122">_lpInterface_</span></span>
  
> <span data-ttu-id="eda42-123">[in] Um ponteiro para o IID (identificador de interface) da interface que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="eda42-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="eda42-124">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="eda42-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="eda42-125">Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="eda42-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="eda42-126">Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="eda42-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="eda42-127">Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="eda42-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="eda42-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eda42-128">_ulFlags_</span></span>
  
> <span data-ttu-id="eda42-129">[in] Uma máscara de bits de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="eda42-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="eda42-130">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="eda42-130">The following flags can be set:</span></span>
    
<span data-ttu-id="eda42-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="eda42-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="eda42-132">Solicita que a entrada seja aberta com as permissões máximas de rede e cliente permitidas.</span><span class="sxs-lookup"><span data-stu-id="eda42-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="eda42-133">Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor do address book tentará abrir a entrada com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="eda42-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="eda42-134">O cliente pode recuperar o nível de acesso concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="eda42-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="eda42-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="eda42-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="eda42-136">Usa apenas o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="eda42-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="eda42-137">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="eda42-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="eda42-138">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="eda42-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="eda42-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="eda42-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="eda42-140">Permite que a chamada seja bem-sucedida, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="eda42-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="eda42-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="eda42-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="eda42-142">Usa somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="eda42-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="eda42-143">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="eda42-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="eda42-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="eda42-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="eda42-145">Solicita que a entrada seja aberta com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="eda42-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="eda42-146">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que a permissão de leitura e gravação foi concedida independentemente de MAPI_MODIFY está definida.</span><span class="sxs-lookup"><span data-stu-id="eda42-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="eda42-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="eda42-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="eda42-148">Não usa o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="eda42-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="eda42-149">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="eda42-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="eda42-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="eda42-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="eda42-151">[out] Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="eda42-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="eda42-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="eda42-152">_lppUnk_</span></span>
  
> <span data-ttu-id="eda42-153">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="eda42-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

