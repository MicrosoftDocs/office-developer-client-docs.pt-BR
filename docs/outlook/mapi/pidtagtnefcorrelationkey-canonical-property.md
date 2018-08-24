---
title: Propriedade canônica PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 760196668ffb3c486803f27b50ff809177e8e6f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588612"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="a11dd-103">Propriedade canônica PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="a11dd-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="a11dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a11dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a11dd-105">Contém um valor que correlaciona um anexo TNEF Transport Neutral Encapsulation Format () com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a11dd-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a11dd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a11dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a11dd-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="a11dd-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="a11dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a11dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a11dd-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="a11dd-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="a11dd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a11dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="a11dd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a11dd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a11dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a11dd-112">Area:</span></span>  <br/> |<span data-ttu-id="a11dd-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="a11dd-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a11dd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a11dd-114">Remarks</span></span>

<span data-ttu-id="a11dd-115">É recomendável que os sub-objetos do anexo TNEF exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a11dd-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="a11dd-116">Esta propriedade determina se ou não um arquivo TNEF entrado pertence à mensagem a que ela está anexada.</span><span class="sxs-lookup"><span data-stu-id="a11dd-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="a11dd-117">Ele é usado principalmente pelos provedores de transporte e gateways.</span><span class="sxs-lookup"><span data-stu-id="a11dd-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="a11dd-118">Em uma mensagem de saída, o provedor de transporte deve compute um valor binário exclusivo para a mensagem ou use um valor existente que satisfaz o requisito de exclusividade, como um identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a11dd-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="a11dd-119">O provedor de transporte deve armazenar esse valor nessa propriedade e, em seguida, chame o método de [ITnef::AddProps](itnef-addprops.md) para encapsulam a ele.</span><span class="sxs-lookup"><span data-stu-id="a11dd-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="a11dd-120">O mesmo valor também deve ser armazenado no envelope transporte em um local definido pelo provedor, como o cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a11dd-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="a11dd-121">Em uma mensagem de entrada, o provedor de transporte deve chamar o método [ITnef::ExtractProps](itnef-extractprops.md) para decapsulate o anexo TNEF e, em seguida, essa propriedade em comparação com o valor armazenado no envelope da transporte.</span><span class="sxs-lookup"><span data-stu-id="a11dd-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="a11dd-122">Se os valores coincidirem, TNEF deve ser processada normalmente, ou seja, todas as propriedades extraídas de anexo TNEF devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="a11dd-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="a11dd-123">Se os valores não coincidirem, todas as propriedades do anexo TNEF devem ser ignoradas.</span><span class="sxs-lookup"><span data-stu-id="a11dd-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="a11dd-124">Se essa propriedade não estiver definida, o arquivo TNEF deve ser considerado ao pertencem a esta mensagem e as outras propriedades extraídas de que ele devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="a11dd-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a11dd-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a11dd-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a11dd-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a11dd-126">Protocol specifications</span></span>

<span data-ttu-id="a11dd-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a11dd-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a11dd-128">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a11dd-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a11dd-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a11dd-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a11dd-130">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="a11dd-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a11dd-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a11dd-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a11dd-132">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a11dd-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a11dd-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a11dd-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a11dd-134">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="a11dd-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a11dd-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a11dd-135">Header files</span></span>

<span data-ttu-id="a11dd-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a11dd-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a11dd-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a11dd-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="a11dd-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a11dd-138">Mapitags.h</span></span>
  
> <span data-ttu-id="a11dd-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a11dd-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a11dd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a11dd-140">See also</span></span>



[<span data-ttu-id="a11dd-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a11dd-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a11dd-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a11dd-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a11dd-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a11dd-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a11dd-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a11dd-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

