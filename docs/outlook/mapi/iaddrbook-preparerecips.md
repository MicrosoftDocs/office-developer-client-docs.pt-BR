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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339218"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="15529-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="15529-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="15529-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15529-105">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="15529-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="15529-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15529-106">Parameters</span></span>

 <span data-ttu-id="15529-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15529-107">_ulFlags_</span></span>
  
> <span data-ttu-id="15529-108">no Uma bitmask de sinalizadores que controla como a entrada é aberta.</span><span class="sxs-lookup"><span data-stu-id="15529-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="15529-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="15529-109">The following flag can be set:</span></span>
    
<span data-ttu-id="15529-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="15529-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="15529-111">Use apenas o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="15529-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="15529-112">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="15529-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="15529-113">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="15529-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="15529-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="15529-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="15529-115">no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades, se houver, que precisam de atualização.</span><span class="sxs-lookup"><span data-stu-id="15529-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="15529-116">O parâmetro _lpSPropTagArray_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="15529-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="15529-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="15529-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="15529-118">no Um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém a lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="15529-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15529-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="15529-119">Return value</span></span>

<span data-ttu-id="15529-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="15529-120">S_OK</span></span> 
  
> <span data-ttu-id="15529-121">A lista de destinatários foi preparada com êxito.</span><span class="sxs-lookup"><span data-stu-id="15529-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15529-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="15529-122">Remarks</span></span>

<span data-ttu-id="15529-123">Os clientes e os provedores de serviços chamam o método **PrepareRecips** para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="15529-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="15529-124">Certifique-se de que todos os destinatários no parâmetro _lpRecipList_ tenham identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="15529-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="15529-125">Certifique-se de que cada destinatário no parâmetro _lpRecipList_ tenha as propriedades listadas no parâmetro _lpSPropTagArray_ e que essas propriedades apareçam no início da lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="15529-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="15529-126">MAPI converte os identificadores de entrada de curto prazo de cada destinatário em identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="15529-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="15529-127">Se necessário, os identificadores de entrada de longo prazo dos destinatários são recuperados do provedor de catálogo de endereços apropriado e qualquer propriedade adicional é solicitada.</span><span class="sxs-lookup"><span data-stu-id="15529-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="15529-128">Em uma entrada de destinatário individual, as propriedades solicitadas são ordenadas primeiro, seguidas por qualquer propriedade que já estava presente para a entrada.</span><span class="sxs-lookup"><span data-stu-id="15529-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="15529-129">Se uma ou mais das propriedades solicitadas no parâmetro _lpSPropTagArray_ não forem tratadas pelo provedor de catálogo de endereços apropriado, seus tipos de propriedade serão definidos como PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="15529-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="15529-130">Seus valores de propriedade serão definidos para MAPI_E_NOT_FOUND ou para outro valor que forneça um motivo mais específico para que as propriedades não estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="15529-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="15529-131">Cada estrutura [SPropValue](spropvalue.md) incluída no parâmetro _lpRecipList_ deve ser alocada separadamente usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) para que ela possa ser liberada individualmente.</span><span class="sxs-lookup"><span data-stu-id="15529-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="15529-132">Para obter informações sobre o PT_ERROR, consulte [tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="15529-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15529-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="15529-133">See also</span></span>



[<span data-ttu-id="15529-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="15529-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="15529-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="15529-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="15529-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="15529-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="15529-137">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="15529-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="15529-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="15529-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="15529-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="15529-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="15529-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="15529-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

