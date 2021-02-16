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
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408891"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="e2cf6-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="e2cf6-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="e2cf6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2cf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2cf6-105">Abre a **entryID** usando o Address Book do Exchange identificado por  _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="e2cf6-106">Esta função funciona de forma semelhante a [IAddrBook::OpenEntry,](iaddrbook-openentry.md) exceto pelo fato de que o uso dessa função garante que [IAddrBook::OpenEntry](iaddrbook-openentry.md) seja aberto usando o provedor do Exchange Address Book esperado.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2cf6-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e2cf6-107">Header file:</span></span>  <br/> |<span data-ttu-id="e2cf6-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e2cf6-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e2cf6-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e2cf6-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2cf6-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2cf6-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2cf6-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e2cf6-111">Called by:</span></span>  <br/> |<span data-ttu-id="e2cf6-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="e2cf6-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e2cf6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2cf6-113">Parameters</span></span>

 <span data-ttu-id="e2cf6-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="e2cf6-115">[in] Um ponteiro para **um emsmdbUID** que identifica o Serviço do Exchange que contém o Exchange Address Book Provider que essa função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="e2cf6-116">Se o identificador de entrada de entrada não for um identificador de entrada do Exchange Address Book Provider, esse parâmetro será ignorado e a chamada de função se comportará como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="e2cf6-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="e2cf6-117">Se esse parâmetro for NULL ou zero MAPIUID, essa função se comportará como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="e2cf6-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="e2cf6-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="e2cf6-119">[in] O livro de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="e2cf6-120">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e2cf6-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="e2cf6-122">[in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="e2cf6-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e2cf6-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="e2cf6-124">[in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="e2cf6-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-125">_lpInterface_</span></span>
  
> <span data-ttu-id="e2cf6-126">[in] Um ponteiro para o IID (identificador de interface) da interface que é usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="e2cf6-127">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="e2cf6-128">Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="e2cf6-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="e2cf6-129">Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e2cf6-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="e2cf6-130">Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="e2cf6-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-131">_ulFlags_</span></span>
  
> <span data-ttu-id="e2cf6-132">[in] Uma bitmask de sinalizadores que controla como a entrada é aberta, os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e2cf6-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="e2cf6-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e2cf6-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="e2cf6-134">Solicita que a entrada seja aberta com as permissões máximas de rede e cliente permitidas.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="e2cf6-135">Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor do address book tentará abrir a entrada com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="e2cf6-136">O cliente pode recuperar o nível de acesso concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="e2cf6-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="e2cf6-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="e2cf6-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="e2cf6-138">Use somente o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="e2cf6-139">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="e2cf6-140">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="e2cf6-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e2cf6-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="e2cf6-142">Permite que a chamada seja bem-sucedida, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="e2cf6-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="e2cf6-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="e2cf6-144">Use somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="e2cf6-145">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="e2cf6-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e2cf6-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="e2cf6-147">Solicita que a entrada seja aberta com permissão de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="e2cf6-148">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que a permissão de leitura e gravação foi concedida independentemente de MAPI_MODIFY está definida.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="e2cf6-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="e2cf6-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="e2cf6-150">Não use o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="e2cf6-151">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="e2cf6-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="e2cf6-153">[out] Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="e2cf6-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="e2cf6-154">_lppUnk_</span></span>
  
> <span data-ttu-id="e2cf6-155">[out] Um ponteiro para um ponteiro da entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="e2cf6-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

