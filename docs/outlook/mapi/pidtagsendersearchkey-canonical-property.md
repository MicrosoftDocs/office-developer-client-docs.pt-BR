---
title: Propriedade canônica PidTagSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderSearchKey
api_type:
- COM
ms.assetid: e15599c5-f40f-46a6-a726-7359efd09ff8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c36d9744bcf5b1126a0fcc90ae6330f2dc8ef0ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386086"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="ed50d-103">Propriedade canônica PidTagSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="ed50d-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ed50d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed50d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed50d-105">Contém a chave de pesquisa do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ed50d-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed50d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ed50d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed50d-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ed50d-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ed50d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ed50d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed50d-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="ed50d-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="ed50d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ed50d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed50d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ed50d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ed50d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ed50d-112">Area:</span></span>  <br/> |<span data-ttu-id="ed50d-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="ed50d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed50d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed50d-114">Remarks</span></span>

<span data-ttu-id="ed50d-115">Essa propriedade é uma das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ed50d-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="ed50d-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar quaisquer valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ed50d-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="ed50d-117">Se nenhum provedor de transporte tem fornecido quaisquer propriedades de endereço do remetente, o MAPI spooler tenta preencher chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed50d-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="ed50d-118">Se nenhum identificadores de entrada foram fornecidos, o MAPI spooler armazena uma chave correspondente à cadeia de caracteres "Desconhecido" nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ed50d-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed50d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed50d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed50d-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ed50d-120">Protocol specifications</span></span>

<span data-ttu-id="ed50d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ed50d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed50d-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ed50d-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ed50d-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="ed50d-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ed50d-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="ed50d-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ed50d-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-130">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="ed50d-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="ed50d-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-132">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="ed50d-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="ed50d-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed50d-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed50d-134">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="ed50d-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed50d-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed50d-135">Header files</span></span>

<span data-ttu-id="ed50d-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed50d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed50d-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ed50d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed50d-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed50d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ed50d-139">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ed50d-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed50d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed50d-140">See also</span></span>



[<span data-ttu-id="ed50d-141">Propriedade canônica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="ed50d-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="ed50d-142">Propriedade canônica PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="ed50d-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="ed50d-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ed50d-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed50d-144">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ed50d-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed50d-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ed50d-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed50d-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ed50d-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

