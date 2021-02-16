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
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341948"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="6cd6c-103">Propriedade canônica PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="6cd6c-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="6cd6c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cd6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cd6c-105">Contém um valor que correlaciona um anexo TNEF (Transport Neutral Encapsulation Format) com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6cd6c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cd6c-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="6cd6c-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="6cd6c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6cd6c-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="6cd6c-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="6cd6c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6cd6c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd6c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6cd6c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-112">Area:</span></span>  <br/> |<span data-ttu-id="6cd6c-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd6c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cd6c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd6c-114">Remarks</span></span>

<span data-ttu-id="6cd6c-115">É recomendável que sub-objetos de anexo TNEF exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="6cd6c-116">Essa propriedade determina se um arquivo TNEF de entrada pertence ou não à mensagem à qual está anexado.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="6cd6c-117">Ele é usado principalmente por provedores de transporte e gateways.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="6cd6c-118">Em uma mensagem de saída, o provedor de transporte deve calcular um valor binário exclusivo dessa mensagem ou usar um valor existente que atenda ao requisito de exclusividade, como um identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="6cd6c-119">O provedor de transporte deve armazenar esse valor nessa propriedade e chamar o método [ITnef::AddProps](itnef-addprops.md) para encapsular esse valor.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="6cd6c-120">O mesmo valor também deve ser armazenado no envelope de transporte em um local definido pelo provedor, como o header da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="6cd6c-121">Em uma mensagem de entrada, o provedor de transporte deve chamar o método [ITnef::ExtractProps](itnef-extractprops.md) para decapsuular o anexo TNEF e comparar essa propriedade com o valor armazenado no envelope de transporte.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="6cd6c-122">Se os valores corresponderem, o TNEF deverá ser processado normalmente, ou seja, todas as propriedades extraídas do anexo TNEF deverão ser usadas.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="6cd6c-123">Se os valores não corresponderem, todas as propriedades do anexo TNEF deverão ser ignoradas.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="6cd6c-124">Se essa propriedade não estiver definida, o arquivo TNEF deverá ser considerado como pertencendo a essa mensagem e as outras propriedades extraídas dela deverão ser usadas.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6cd6c-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cd6c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cd6c-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6cd6c-126">Protocol specifications</span></span>

<span data-ttu-id="6cd6c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-128">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6cd6c-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-130">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6cd6c-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-132">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6cd6c-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-134">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cd6c-135">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="6cd6c-135">Header files</span></span>

<span data-ttu-id="6cd6c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cd6c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cd6c-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="6cd6c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6cd6c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="6cd6c-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6cd6c-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cd6c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cd6c-140">See also</span></span>



[<span data-ttu-id="6cd6c-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd6c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cd6c-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd6c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cd6c-143">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd6c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cd6c-144">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6cd6c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

