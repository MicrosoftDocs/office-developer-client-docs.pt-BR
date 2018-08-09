---
title: Propriedade canônica PidTagSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b97446c946c31ca8b55ce6c412814b48f4ee363c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769992"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a><span data-ttu-id="82540-103">Propriedade canônica PidTagSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="82540-103">PidTagSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="82540-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82540-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82540-105">Contém o endereço de email do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="82540-105">Contains the message sender's email address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82540-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="82540-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82540-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="82540-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="82540-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="82540-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82540-109">0x0C1F</span><span class="sxs-lookup"><span data-stu-id="82540-109">0x0C1F</span></span>  <br/> |
|<span data-ttu-id="82540-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="82540-110">Data type:</span></span>  <br/> |<span data-ttu-id="82540-111">PT_UNICOIDE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="82540-111">PT_UNICOIDE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="82540-112">Área:</span><span class="sxs-lookup"><span data-stu-id="82540-112">Area:</span></span>  <br/> |<span data-ttu-id="82540-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="82540-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82540-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="82540-114">Remarks</span></span>

<span data-ttu-id="82540-115">Essas propriedades são exemplos das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="82540-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="82540-116">Devem ser definidas pelo provedor de transporte de saída, que nunca deve propagar quaisquer valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="82540-116">They must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="82540-117">Se nenhum provedor de transporte tem fornecido quaisquer propriedades de endereço do remetente, o MAPI spooler tenta preencher chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="82540-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="82540-118">Se nenhum identificadores de entrada foram fornecidos, o MAPI spooler armazena "Desconhecido" em todas as propriedades de endereço de remetente do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="82540-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82540-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="82540-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82540-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="82540-120">Protocol specifications</span></span>

<span data-ttu-id="82540-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="82540-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82540-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="82540-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="82540-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="82540-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="82540-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="82540-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="82540-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-130">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="82540-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="82540-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-132">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="82540-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="82540-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82540-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82540-134">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="82540-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82540-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82540-135">Header files</span></span>

<span data-ttu-id="82540-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82540-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="82540-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="82540-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="82540-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82540-138">Mapitags.h</span></span>
  
> <span data-ttu-id="82540-139">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="82540-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82540-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="82540-140">See also</span></span>



[<span data-ttu-id="82540-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="82540-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82540-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="82540-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82540-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="82540-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82540-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="82540-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
