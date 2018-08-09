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
ms.openlocfilehash: ea0e2b753212acc48c56240b3a72b7f22954802a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769998"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="06f79-103">Propriedade canônica PidTagSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="06f79-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="06f79-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06f79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06f79-105">Contém a chave de pesquisa do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="06f79-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06f79-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="06f79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06f79-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="06f79-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="06f79-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="06f79-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06f79-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="06f79-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="06f79-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="06f79-110">Data type:</span></span>  <br/> |<span data-ttu-id="06f79-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="06f79-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="06f79-112">Área:</span><span class="sxs-lookup"><span data-stu-id="06f79-112">Area:</span></span>  <br/> |<span data-ttu-id="06f79-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="06f79-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06f79-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="06f79-114">Remarks</span></span>

<span data-ttu-id="06f79-115">Essa propriedade é uma das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="06f79-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="06f79-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar quaisquer valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="06f79-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="06f79-117">Se nenhum provedor de transporte tem fornecido quaisquer propriedades de endereço do remetente, o MAPI spooler tenta preencher chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="06f79-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="06f79-118">Se nenhum identificadores de entrada foram fornecidos, o MAPI spooler armazena uma chave correspondente à cadeia de caracteres "Desconhecido" nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="06f79-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06f79-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="06f79-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06f79-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="06f79-120">Protocol specifications</span></span>

<span data-ttu-id="06f79-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="06f79-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06f79-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="06f79-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="06f79-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="06f79-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="06f79-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="06f79-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="06f79-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-130">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="06f79-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="06f79-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-132">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="06f79-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="06f79-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f79-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f79-134">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="06f79-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06f79-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06f79-135">Header files</span></span>

<span data-ttu-id="06f79-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06f79-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="06f79-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="06f79-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="06f79-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06f79-138">Mapitags.h</span></span>
  
> <span data-ttu-id="06f79-139">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="06f79-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06f79-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="06f79-140">See also</span></span>



[<span data-ttu-id="06f79-141">Propriedade canônica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="06f79-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="06f79-142">Propriedade canônica PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="06f79-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="06f79-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="06f79-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06f79-144">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="06f79-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06f79-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="06f79-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06f79-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="06f79-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

