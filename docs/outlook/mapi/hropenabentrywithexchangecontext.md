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
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434050"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="bac43-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="bac43-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="bac43-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bac43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bac43-105">Abre a **EntryID** usando o catálogo de endereços do Exchange identificado pelo **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="bac43-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="bac43-106">Essa função funciona de forma semelhante à [IAddrBook::D etails](iaddrbook-details.md) , exceto que usar essa função garante que o [IAddrBook:: OpenEntry](iaddrbook-openentry.md) seja aberto usando o provedor de catálogo de endereços do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="bac43-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bac43-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bac43-107">Header file:</span></span>  <br/> |<span data-ttu-id="bac43-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="bac43-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="bac43-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bac43-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="bac43-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="bac43-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="bac43-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="bac43-111">Called by:</span></span>  <br/> |<span data-ttu-id="bac43-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="bac43-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="bac43-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bac43-113">Parameters</span></span>

 <span data-ttu-id="bac43-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="bac43-114">_pmsess_</span></span>
  
> <span data-ttu-id="bac43-115">no O **IMAPISession**conectado.</span><span class="sxs-lookup"><span data-stu-id="bac43-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="bac43-116">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="bac43-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bac43-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="bac43-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="bac43-118">no Um ponteiro para um **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que essa função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="bac43-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="bac43-119">Se o identificador de entrada de entrada não for um identificador de entrada do provedor de catálogo de endereços do Exchange, este parâmetro será ignorado e a chamada de função se comformará como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="bac43-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="bac43-120">Se esse parâmetro for nulo ou um MAPIUID zero, essa função se comformará como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="bac43-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="bac43-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="bac43-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="bac43-122">no O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="bac43-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="bac43-123">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="bac43-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bac43-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bac43-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="bac43-125">no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="bac43-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bac43-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bac43-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="bac43-127">no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="bac43-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="bac43-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bac43-128">_ulFlags_</span></span>
  
> <span data-ttu-id="bac43-129">no Uma bitmask de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="bac43-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="bac43-130">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="bac43-130">The following flags can be set:</span></span>
    
<span data-ttu-id="bac43-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bac43-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="bac43-132">Solicita que a entrada seja aberta com o máximo permitido de rede e permissões de cliente.</span><span class="sxs-lookup"><span data-stu-id="bac43-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="bac43-133">Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor de catálogo de endereços tentará abrir a entrada com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="bac43-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="bac43-134">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="bac43-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="bac43-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="bac43-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="bac43-136">Usa apenas o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="bac43-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="bac43-137">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="bac43-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="bac43-138">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="bac43-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="bac43-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bac43-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="bac43-140">Permite que a chamada seja bem-sucedida, possivelmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="bac43-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="bac43-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="bac43-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="bac43-142">Usa somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="bac43-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="bac43-143">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="bac43-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="bac43-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bac43-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="bac43-145">Solicita que a entrada seja aberta com permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="bac43-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="bac43-146">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem supor que a permissão de leitura e gravação tenha sido concedida independentemente de o MAPI_MODIFY ser definido.</span><span class="sxs-lookup"><span data-stu-id="bac43-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="bac43-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="bac43-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="bac43-148">Não usa o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="bac43-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="bac43-149">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="bac43-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

