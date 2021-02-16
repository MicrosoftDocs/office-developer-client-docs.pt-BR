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
ms.openlocfilehash: 82c0e386ab9231d1066dbdc4456c31031d2409c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359161"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a><span data-ttu-id="ba75d-103">Propriedade canônica PidTagSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ba75d-103">PidTagSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="ba75d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba75d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba75d-105">Contém o endereço de email do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ba75d-105">Contains the message sender's email address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba75d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ba75d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba75d-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="ba75d-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="ba75d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ba75d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba75d-109">0x0C1F</span><span class="sxs-lookup"><span data-stu-id="ba75d-109">0x0C1F</span></span>  <br/> |
|<span data-ttu-id="ba75d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ba75d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba75d-111">PT_UNICOIDE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ba75d-111">PT_UNICOIDE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ba75d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ba75d-112">Area:</span></span>  <br/> |<span data-ttu-id="ba75d-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="ba75d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba75d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba75d-114">Remarks</span></span>

<span data-ttu-id="ba75d-115">Essas propriedades são exemplos das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ba75d-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="ba75d-116">Eles devem ser definidos pelo provedor de transporte de saída, que nunca deve propagar valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba75d-116">They must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="ba75d-117">Se nenhum provedor de transporte tiver fornecido qualquer propriedade de endereço do remetente, o spooler MAPI tentará preenchê-las chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ba75d-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="ba75d-118">Se nenhum identificador de entrada tiver sido fornecido, o spooler MAPI armazenará "Desconhecido" em todas as propriedades de endereço do remetente do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="ba75d-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ba75d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba75d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ba75d-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ba75d-120">Protocol specifications</span></span>

<span data-ttu-id="ba75d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ba75d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ba75d-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ba75d-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ba75d-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-126">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="ba75d-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ba75d-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="ba75d-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ba75d-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-130">Especifica as propriedades e operações que são permitidas para postagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="ba75d-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="ba75d-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-132">Especifica as propriedades e operações que são permitidas para contatos e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="ba75d-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="ba75d-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba75d-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba75d-134">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ba75d-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ba75d-135">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ba75d-135">Header files</span></span>

<span data-ttu-id="ba75d-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba75d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba75d-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ba75d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba75d-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba75d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ba75d-139">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ba75d-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba75d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba75d-140">See also</span></span>



[<span data-ttu-id="ba75d-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ba75d-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba75d-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ba75d-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba75d-143">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ba75d-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba75d-144">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ba75d-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

