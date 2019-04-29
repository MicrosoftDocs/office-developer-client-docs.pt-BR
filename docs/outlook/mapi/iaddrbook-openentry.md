---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Última modificação: 1 de fevereiro de 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434162"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="64e3c-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="64e3c-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="64e3c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64e3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64e3c-105">Abre uma entrada do catálogo de endereços e retorna um ponteiro para uma interface que pode ser usada para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="64e3c-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="64e3c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64e3c-106">Parameters</span></span>

<span data-ttu-id="64e3c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="64e3c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="64e3c-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="64e3c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="64e3c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="64e3c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="64e3c-110">no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="64e3c-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="64e3c-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="64e3c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="64e3c-112">no Um ponteiro para o identificador de interface (IID) da interface a ser usado para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="64e3c-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="64e3c-113">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="64e3c-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="64e3c-114">Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="64e3c-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="64e3c-115">Para listas de distribuição, é [IDistList: IMAPIContainer](idistlistimapicontainer.md) e para contêiners, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="64e3c-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="64e3c-116">Os chamadores podem definir _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="64e3c-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="64e3c-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64e3c-117">_ulFlags_</span></span>
  
> <span data-ttu-id="64e3c-118">no Uma bitmask de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="64e3c-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="64e3c-119">Os seguintes sinalizadores podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="64e3c-119">The following flags can be set.</span></span>
    
<span data-ttu-id="64e3c-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="64e3c-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="64e3c-121">Solicita que a entrada seja aberta com o máximo permitido de rede e permissões de cliente.</span><span class="sxs-lookup"><span data-stu-id="64e3c-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="64e3c-122">Por exemplo, se o cliente tiver permissão de leitura/gravação, o provedor de catálogo de endereços deverá tentar abrir a entrada com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="64e3c-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="64e3c-123">O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps da entrada aberta e recuperando a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64e3c-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="64e3c-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="64e3c-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="64e3c-125">Abre uma entrada do catálogo de endereços e a acessa somente do cache.</span><span class="sxs-lookup"><span data-stu-id="64e3c-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="64e3c-126">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="64e3c-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="64e3c-127">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="64e3c-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="64e3c-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="64e3c-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="64e3c-129">Permite que a chamada seja bem-sucedida, possivelmente antes que a entrada esteja totalmente aberta e disponível, o que significa que chamadas posteriores à entrada podem retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="64e3c-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="64e3c-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="64e3c-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="64e3c-131">Use somente a GAL para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="64e3c-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="64e3c-132">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="64e3c-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="64e3c-133">O _parâmetroulflags_ MAPI_GAL_ONLY pode não estar definido no arquivo de cabeçalho baixável que você tem atualmente, e, nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="64e3c-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="64e3c-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="64e3c-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="64e3c-135">Solicita que a entrada seja aberta com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="64e3c-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="64e3c-136">Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem supor que a permissão de leitura/gravação tenha sido concedida independentemente de o MAPI_MODIFY ser definido.</span><span class="sxs-lookup"><span data-stu-id="64e3c-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="64e3c-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="64e3c-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="64e3c-138">Não use o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="64e3c-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="64e3c-139">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="64e3c-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="64e3c-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="64e3c-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="64e3c-141">bota Um ponteiro para o tipo de entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="64e3c-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="64e3c-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="64e3c-142">_lppUnk_</span></span>
  
> <span data-ttu-id="64e3c-143">bota Um ponteiro para um ponteiro para a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="64e3c-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="64e3c-144">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="64e3c-144">Return value</span></span>

<span data-ttu-id="64e3c-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="64e3c-145">S_OK</span></span> 
  
> <span data-ttu-id="64e3c-146">A entrada foi aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="64e3c-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="64e3c-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="64e3c-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="64e3c-148">Foi feita uma tentativa de abrir uma entrada para a qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="64e3c-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="64e3c-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="64e3c-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="64e3c-150">A entrada representada por _lpEntryID_ não existe.</span><span class="sxs-lookup"><span data-stu-id="64e3c-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="64e3c-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="64e3c-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="64e3c-152">O identificador de entrada especificado em _lpEntryID_ não é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="64e3c-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="64e3c-153">Esse valor normalmente é retornado se o provedor de catálogo de endereços responsável pela entrada correspondente não estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="64e3c-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="64e3c-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="64e3c-154">Remarks</span></span>

<span data-ttu-id="64e3c-155">Os clientes e os provedores de serviços chamam o método **IAddrBook:: OpenEntry** para abrir uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="64e3c-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="64e3c-156">O MAPI encaminha a chamada para o provedor de catálogo de endereços apropriado, com base na estrutura [MAPIUID](mapiuid.md) incluída no identificador de entrada passado no parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="64e3c-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="64e3c-157">O provedor de catálogo de endereços abre a entrada como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ seja definido.</span><span class="sxs-lookup"><span data-stu-id="64e3c-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="64e3c-158">No enTanto, esses sinalizadores são sugestões.</span><span class="sxs-lookup"><span data-stu-id="64e3c-158">However, these flags are suggestions.</span></span> <span data-ttu-id="64e3c-159">Se o provedor de catálogo de endereços não permitir a modificação da entrada solicitada, ele retornará MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="64e3c-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="64e3c-160">O parâmetro _lpInterface_ indica qual interface deve ser usada para acessar a entrada aberta.</span><span class="sxs-lookup"><span data-stu-id="64e3c-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="64e3c-161">Passar NULL no _lpInterface_ indica que a interface MAPI padrão para esse tipo de entrada deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="64e3c-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="64e3c-162">Como o provedor de catálogo de endereços pode retornar uma interface diferente da sugerida pelo parâmetro _lpInterface_ , o chamador deve verificar o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o que era esperado.</span><span class="sxs-lookup"><span data-stu-id="64e3c-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="64e3c-163">Se o tipo de objeto não for do tipo esperado, o chamador poderá converter o parâmetro _lppUnk_ para um tipo mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="64e3c-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64e3c-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="64e3c-164">See also</span></span>

- [<span data-ttu-id="64e3c-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="64e3c-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

