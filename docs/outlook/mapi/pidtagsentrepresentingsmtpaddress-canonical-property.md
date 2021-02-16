---
title: Propriedade canônica PidTagSentRepresentingSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341934"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="cbcf7-103">Propriedade canônica PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="cbcf7-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="cbcf7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbcf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbcf7-105">Contém o endereço de email SMTP para o usuário de mensagens representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbcf7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cbcf7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbcf7-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="cbcf7-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="cbcf7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cbcf7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbcf7-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="cbcf7-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="cbcf7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cbcf7-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbcf7-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cbcf7-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cbcf7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cbcf7-112">Area:</span></span>  <br/> |<span data-ttu-id="cbcf7-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="cbcf7-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbcf7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbcf7-114">Remarks</span></span>

<span data-ttu-id="cbcf7-115">Essa propriedade é um exemplo das propriedades de endereço do usuário de mensagens que está sendo representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="cbcf7-116">Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades do remetente representado para os valores desse cliente.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="cbcf7-117">Um usuário de mensagens que envia em seu próprio nome normalmente deixa as propriedades do remetente representadas desaperadas.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="cbcf7-118">O provedor de transporte de saída deve sempre deixar essa propriedade inalterada se tiver sido definida pelo cliente de envio.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="cbcf7-119">Se não for definido, o provedor de transporte deverá defini-lo como a propriedade **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) na cópia de saída da mensagem e deixá-la desa definida na cópia local.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cbcf7-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbcf7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbcf7-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cbcf7-121">Protocol specifications</span></span>

<span data-ttu-id="cbcf7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-123">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cbcf7-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-125">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="cbcf7-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-127">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="cbcf7-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-129">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="cbcf7-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-131">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="cbcf7-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-133">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="cbcf7-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-135">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="cbcf7-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcf7-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcf7-137">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbcf7-138">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="cbcf7-138">Header files</span></span>

<span data-ttu-id="cbcf7-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbcf7-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbcf7-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="cbcf7-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cbcf7-141">Mapitags.h</span></span>
  
> <span data-ttu-id="cbcf7-142">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbcf7-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbcf7-143">See also</span></span>



[<span data-ttu-id="cbcf7-144">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cbcf7-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbcf7-145">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="cbcf7-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbcf7-146">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cbcf7-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbcf7-147">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cbcf7-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

