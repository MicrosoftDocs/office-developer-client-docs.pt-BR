---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563874"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="7dfe9-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="7dfe9-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="7dfe9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dfe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dfe9-105">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="7dfe9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dfe9-106">Parameters</span></span>

 <span data-ttu-id="7dfe9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7dfe9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7dfe9-108">[in] Uma bitmask dos sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="7dfe9-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7dfe9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7dfe9-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="7dfe9-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="7dfe9-111">Use somente o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="7dfe9-112">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="7dfe9-113">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="7dfe9-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="7dfe9-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="7dfe9-115">[in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades, se houver, que requeiram a atualização.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="7dfe9-116">O parâmetro _lpSPropTagArray_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="7dfe9-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="7dfe9-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="7dfe9-118">[in] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém a lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7dfe9-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7dfe9-119">Return value</span></span>

<span data-ttu-id="7dfe9-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="7dfe9-120">S_OK</span></span> 
  
> <span data-ttu-id="7dfe9-121">A lista de destinatários foi preparada com êxito.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7dfe9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dfe9-122">Remarks</span></span>

<span data-ttu-id="7dfe9-123">Clientes e provedores de serviços de chamar o método de **PrepareRecips** para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7dfe9-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="7dfe9-124">Certifique-se de que todos os destinatários no parâmetro _lpRecipList_ tenham identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="7dfe9-125">Certifique-se de que cada destinatário no parâmetro _lpRecipList_ tem as propriedades listadas no parâmetro _lpSPropTagArray_ e que essas propriedades serão exibidas no início da lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="7dfe9-126">MAPI converte os identificadores de entrada de curto prazo de cada destinatário aos identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="7dfe9-127">Se necessário, longo prazo identificadores de entrada dos destinatários são recuperados do provedor de catálogo de endereço apropriado e as propriedades adicionais solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="7dfe9-128">Em uma entrada individual de destinatário, as propriedades solicitadas são ordenadas primeiro, seguido de quaisquer propriedades que já estavam presentes para a entrada.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="7dfe9-129">Se uma ou mais das propriedades solicitadas no parâmetro _lpSPropTagArray_ não são tratados pelo provedor de catálogo de endereço apropriado, seus tipos de propriedade serão definidos para PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="7dfe9-130">Seus valores de propriedade serão definidos para a E_NOT_FOUND ou a outro valor que dá um motivo mais específico, por que as propriedades não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="7dfe9-131">Cada estrutura [SPropValue](spropvalue.md) incluída no parâmetro _lpRecipList_ deve ser alocada separadamente usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) para que ela pode ser liberada individualmente.</span><span class="sxs-lookup"><span data-stu-id="7dfe9-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="7dfe9-132">Para obter informações sobre PT_ERROR, consulte [Tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7dfe9-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dfe9-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dfe9-133">See also</span></span>



[<span data-ttu-id="7dfe9-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="7dfe9-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="7dfe9-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7dfe9-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="7dfe9-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="7dfe9-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="7dfe9-137">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="7dfe9-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="7dfe9-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7dfe9-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="7dfe9-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7dfe9-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="7dfe9-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7dfe9-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

