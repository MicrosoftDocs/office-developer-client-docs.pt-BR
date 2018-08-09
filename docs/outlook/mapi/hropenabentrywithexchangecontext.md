---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766798"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="b3d8e-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="b3d8e-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="b3d8e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3d8e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3d8e-105">Abre a **entryID** usando o catálogo de endereços do Exchange identificado pela **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="b3d8e-106">Essa função funcionamento é semelhante ao [IAddrBook::Details](iaddrbook-details.md) , exceto pelo fato usando esta função garante que o [IAddrBook::OpenEntry](iaddrbook-openentry.md) é aberto usando o provedor de catálogo de endereços do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3d8e-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b3d8e-107">Header file:</span></span>  <br/> |<span data-ttu-id="b3d8e-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="b3d8e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="b3d8e-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b3d8e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3d8e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3d8e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3d8e-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b3d8e-111">Called by:</span></span>  <br/> |<span data-ttu-id="b3d8e-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b3d8e-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b3d8e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3d8e-113">Parameters</span></span>

 <span data-ttu-id="b3d8e-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="b3d8e-114">_pmsess_</span></span>
  
> <span data-ttu-id="b3d8e-115">[in] O conectado **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="b3d8e-116">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="b3d8e-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="b3d8e-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="b3d8e-118">[in] Um ponteiro para uma **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que esta função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="b3d8e-119">Se o identificador de entrada de entrada não é um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a chamada de função se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="b3d8e-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="b3d8e-120">Se esse parâmetro for NULL ou um zero MAPIUID, essa função se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="b3d8e-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="b3d8e-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="b3d8e-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="b3d8e-122">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="b3d8e-123">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="b3d8e-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b3d8e-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="b3d8e-125">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b3d8e-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b3d8e-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b3d8e-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="b3d8e-127">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="b3d8e-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3d8e-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b3d8e-129">[in] Uma bitmask dos sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="b3d8e-130">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b3d8e-130">The following flags can be set:</span></span>
    
<span data-ttu-id="b3d8e-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b3d8e-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="b3d8e-132">Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="b3d8e-133">Por exemplo, se o cliente tem de leitura e permissão de gravação, o provedor de catálogo de endereços tenta abrir a entrada com a leitura e a permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="b3d8e-134">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="b3d8e-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="b3d8e-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b3d8e-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="b3d8e-136">Usa apenas o catálogo de endereços offline para realizar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="b3d8e-137">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="b3d8e-138">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b3d8e-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b3d8e-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="b3d8e-140">Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes à entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="b3d8e-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="b3d8e-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="b3d8e-142">Usa apenas a GAL para realizar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="b3d8e-143">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b3d8e-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b3d8e-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="b3d8e-145">Solicitações que a entrada ser aberto com leia e permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="b3d8e-146">Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que ler e gravar a permissão foi concedida independentemente MAPI_MODIFY é definida.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="b3d8e-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="b3d8e-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="b3d8e-148">Não usa o catálogo de endereços offline para executar a resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="b3d8e-149">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

