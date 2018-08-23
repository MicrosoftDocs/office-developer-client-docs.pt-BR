---
title: Propriedade canônica PidTagSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderAddressType
api_type:
- COM
ms.assetid: ad7f49ac-6fe8-4037-90f3-8dabd5648bed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f304f8eb8166d94af6f098dfdef89af9ff9ad7c3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584790"
---
# <a name="pidtagsenderaddresstype-canonical-property"></a><span data-ttu-id="0ce24-103">Propriedade canônica PidTagSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="0ce24-103">PidTagSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="0ce24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ce24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ce24-105">Contém o tipo de endereço de email do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ce24-105">Contains the message sender's email address type.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ce24-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0ce24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ce24-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="0ce24-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="0ce24-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0ce24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ce24-109">0x0C1E</span><span class="sxs-lookup"><span data-stu-id="0ce24-109">0x0C1E</span></span>  <br/> |
|<span data-ttu-id="0ce24-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0ce24-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ce24-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0ce24-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0ce24-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0ce24-112">Area:</span></span>  <br/> |<span data-ttu-id="0ce24-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="0ce24-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ce24-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ce24-114">Remarks</span></span>

<span data-ttu-id="0ce24-115">Essas propriedades são exemplos das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ce24-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="0ce24-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar quaisquer valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0ce24-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="0ce24-117">Se nenhum provedor de transporte tem fornecido quaisquer propriedades de endereço do remetente, o MAPI spooler tenta preencher chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ce24-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="0ce24-118">Se nenhum identificadores de entrada foram fornecidos, o MAPI spooler armazena "Desconhecido" em todas as propriedades de endereço de remetente do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="0ce24-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ce24-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ce24-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ce24-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0ce24-120">Protocol specifications</span></span>

<span data-ttu-id="0ce24-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0ce24-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ce24-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="0ce24-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0ce24-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="0ce24-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0ce24-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="0ce24-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0ce24-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-130">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="0ce24-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="0ce24-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-132">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="0ce24-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="0ce24-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ce24-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ce24-134">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="0ce24-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ce24-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0ce24-135">Header files</span></span>

<span data-ttu-id="0ce24-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ce24-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ce24-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0ce24-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ce24-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ce24-138">Mapitags.h</span></span>
  
> <span data-ttu-id="0ce24-139">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="0ce24-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ce24-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ce24-140">See also</span></span>



[<span data-ttu-id="0ce24-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce24-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ce24-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0ce24-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ce24-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce24-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ce24-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0ce24-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

