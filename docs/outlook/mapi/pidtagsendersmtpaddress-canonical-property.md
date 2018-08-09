---
title: Propriedade canônica PidTagSenderSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d69fb4423fca12134b4401907a16636562557cfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770001"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="c0705-103">Propriedade canônica PidTagSenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c0705-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="c0705-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0705-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0705-105">Contém o formato do endereço de email do protocolo de transporte de email simples (SMTP) do proprietário da caixa de correio do envio.</span><span class="sxs-lookup"><span data-stu-id="c0705-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0705-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c0705-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0705-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="c0705-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="c0705-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c0705-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0705-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="c0705-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="c0705-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c0705-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0705-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c0705-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c0705-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c0705-112">Area:</span></span>  <br/> |<span data-ttu-id="c0705-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="c0705-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0705-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0705-114">Remarks</span></span>

<span data-ttu-id="c0705-115">Essa propriedade é um exemplo das propriedades endereço de remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0705-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="c0705-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar quaisquer valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c0705-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="c0705-117">Se nenhum provedor de transporte tem fornecido quaisquer propriedades de endereço do remetente, o MAPI spooler tenta preencher chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0705-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="c0705-118">Se nenhum identificadores de entrada foram fornecidos, o MAPI spooler armazena "Desconhecido" em todas as propriedades de endereço de remetente do tipo PT_UNICODE ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="c0705-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c0705-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0705-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0705-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c0705-120">Protocol specifications</span></span>

<span data-ttu-id="c0705-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-122">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c0705-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0705-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c0705-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c0705-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="c0705-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c0705-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="c0705-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c0705-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-130">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="c0705-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="c0705-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-132">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="c0705-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="c0705-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0705-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0705-134">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="c0705-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0705-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c0705-135">Header files</span></span>

<span data-ttu-id="c0705-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0705-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0705-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c0705-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0705-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0705-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c0705-139">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c0705-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0705-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0705-140">See also</span></span>



[<span data-ttu-id="c0705-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c0705-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0705-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c0705-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0705-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c0705-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0705-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c0705-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

