---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ed68e1fdb7fb990a2c19aa0bd263439c0966231d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578203"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="a5633-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="a5633-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="a5633-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5633-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5633-105">Abre a **entryID** usando o catálogo de endereços do Exchange identificado pela _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="a5633-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="a5633-106">Essa função funciona de maneira semelhante para [IAddrBook::OpenEntry](iaddrbook-openentry.md) , exceto que o uso da função garante que [IAddrBook::OpenEntry](iaddrbook-openentry.md) é aberto usando o provedor de catálogo de endereços do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="a5633-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5633-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a5633-107">Header file:</span></span>  <br/> |<span data-ttu-id="a5633-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a5633-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a5633-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a5633-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a5633-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5633-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a5633-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a5633-111">Called by:</span></span>  <br/> |<span data-ttu-id="a5633-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a5633-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a5633-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5633-113">Parameters</span></span>

 <span data-ttu-id="a5633-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="a5633-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="a5633-115">[in] Um ponteiro para uma **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que esta função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5633-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a5633-116">Se o identificador de entrada de entrada não é um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a chamada de função se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a5633-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a5633-117">Se esse parâmetro for NULL ou um zero MAPIUID, essa função se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a5633-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a5633-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a5633-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="a5633-119">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5633-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a5633-120">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a5633-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a5633-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a5633-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="a5633-122">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a5633-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a5633-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a5633-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="a5633-124">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="a5633-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="a5633-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a5633-125">_lpInterface_</span></span>
  
> <span data-ttu-id="a5633-126">[in] Um ponteiro para o identificador de interface (IID) da interface do que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="a5633-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="a5633-127">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="a5633-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a5633-128">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a5633-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a5633-129">Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a5633-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a5633-130">Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="a5633-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a5633-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5633-131">_ulFlags_</span></span>
  
> <span data-ttu-id="a5633-132">[in] Uma bitmask dos sinalizadores que controla o como a entrada é aberta, sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a5633-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="a5633-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a5633-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="a5633-134">Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas.</span><span class="sxs-lookup"><span data-stu-id="a5633-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="a5633-135">Por exemplo, se o cliente tem de leitura e permissão de gravação, o provedor de catálogo de endereços tenta abrir a entrada com a leitura e a permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="a5633-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="a5633-136">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="a5633-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="a5633-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="a5633-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="a5633-138">Use somente o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="a5633-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="a5633-139">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="a5633-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="a5633-140">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a5633-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="a5633-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a5633-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="a5633-142">Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes à entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="a5633-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="a5633-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="a5633-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="a5633-144">Use somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="a5633-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="a5633-145">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a5633-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="a5633-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a5633-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="a5633-147">Solicitações que a entrada ser aberto com leia e permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="a5633-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="a5633-148">Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que ler e gravar a permissão foi concedida independentemente MAPI_MODIFY é definida.</span><span class="sxs-lookup"><span data-stu-id="a5633-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="a5633-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="a5633-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="a5633-150">Não use o catálogo de endereços offline para executar a resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="a5633-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="a5633-151">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a5633-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="a5633-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a5633-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="a5633-153">[out] Um ponteiro para o tipo da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="a5633-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a5633-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a5633-154">_lppUnk_</span></span>
  
> <span data-ttu-id="a5633-155">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="a5633-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

