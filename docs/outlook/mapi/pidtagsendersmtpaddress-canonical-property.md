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
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342627"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="68452-103">Propriedade canônica PidTagSenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="68452-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="68452-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68452-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68452-105">Contém o formato do endereço de email SMTP do proprietário da caixa de correio de envio.</span><span class="sxs-lookup"><span data-stu-id="68452-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68452-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="68452-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68452-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="68452-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="68452-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="68452-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68452-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="68452-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="68452-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="68452-110">Data type:</span></span>  <br/> |<span data-ttu-id="68452-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="68452-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="68452-112">Área:</span><span class="sxs-lookup"><span data-stu-id="68452-112">Area:</span></span>  <br/> |<span data-ttu-id="68452-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="68452-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68452-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="68452-114">Remarks</span></span>

<span data-ttu-id="68452-115">Essa propriedade é um exemplo das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="68452-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="68452-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="68452-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="68452-117">Se nenhum provedor de transporte tiver fornecido qualquer propriedade de endereço do remetente, o spooler MAPI tentará preenchê-las chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="68452-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="68452-118">Se nenhum identificador de entrada tiver sido fornecido, o spooler MAPI armazenará "Desconhecido" em todas as propriedades de endereço do remetente do tipo PT_UNICODE ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="68452-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="68452-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="68452-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68452-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="68452-120">Protocol specifications</span></span>

<span data-ttu-id="68452-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-122">Fornece referências a especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="68452-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68452-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="68452-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="68452-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-126">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="68452-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="68452-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="68452-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="68452-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-130">Especifica as propriedades e operações que são permitidas para postagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="68452-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="68452-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-132">Especifica as propriedades e operações que são permitidas para contatos e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="68452-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="68452-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68452-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68452-134">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="68452-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68452-135">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="68452-135">Header files</span></span>

<span data-ttu-id="68452-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68452-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="68452-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="68452-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="68452-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="68452-138">Mapitags.h</span></span>
  
> <span data-ttu-id="68452-139">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="68452-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68452-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="68452-140">See also</span></span>



[<span data-ttu-id="68452-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="68452-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68452-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="68452-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68452-143">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="68452-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68452-144">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="68452-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

