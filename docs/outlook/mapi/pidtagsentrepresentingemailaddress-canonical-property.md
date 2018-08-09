---
title: Propriedade canônica PidTagSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1ed8797a9f9de223d8ec15bc0eae963ff1e93be4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770016"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="24b18-103">Propriedade canônica PidTagSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="24b18-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="24b18-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24b18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24b18-105">Contém o endereço de email para o usuário de mensagens que é representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="24b18-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24b18-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="24b18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24b18-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="24b18-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="24b18-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="24b18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24b18-109">0x0065</span><span class="sxs-lookup"><span data-stu-id="24b18-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="24b18-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="24b18-110">Data type:</span></span>  <br/> |<span data-ttu-id="24b18-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="24b18-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="24b18-112">Área:</span><span class="sxs-lookup"><span data-stu-id="24b18-112">Area:</span></span>  <br/> |<span data-ttu-id="24b18-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="24b18-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24b18-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="24b18-114">Remarks</span></span>

<span data-ttu-id="24b18-115">Essas propriedades são exemplos das propriedades de endereço para o usuário de mensagens está sendo representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="24b18-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="24b18-116">Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades de remetente representado para os valores para que o cliente.</span><span class="sxs-lookup"><span data-stu-id="24b18-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="24b18-117">Um usuário de mensagens enviando em seu próprio nome geralmente deixa as propriedades de remetente representado não definidas.</span><span class="sxs-lookup"><span data-stu-id="24b18-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="24b18-118">O provedor de transporte de saída deve sempre deixar essas propriedades inalteradas se ele tiver sido definido pelo cliente de envio.</span><span class="sxs-lookup"><span data-stu-id="24b18-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="24b18-119">Se ela foi removida, o provedor de transporte deve defini-la como a propriedade **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) na cópia de saída da mensagem e deixá-lo não definidas na cópia local.</span><span class="sxs-lookup"><span data-stu-id="24b18-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="24b18-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="24b18-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24b18-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="24b18-121">Protocol specifications</span></span>

<span data-ttu-id="24b18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="24b18-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24b18-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-125">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="24b18-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="24b18-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-127">Especifica as propriedades e operações que representam os itens RSS.</span><span class="sxs-lookup"><span data-stu-id="24b18-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="24b18-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-129">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="24b18-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="24b18-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-131">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="24b18-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="24b18-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-133">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="24b18-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="24b18-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-135">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="24b18-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="24b18-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b18-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b18-137">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="24b18-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24b18-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="24b18-138">Header files</span></span>

<span data-ttu-id="24b18-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24b18-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="24b18-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="24b18-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="24b18-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24b18-141">Mapitags.h</span></span>
  
> <span data-ttu-id="24b18-142">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="24b18-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24b18-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="24b18-143">See also</span></span>



[<span data-ttu-id="24b18-144">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="24b18-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24b18-145">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="24b18-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24b18-146">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="24b18-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24b18-147">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="24b18-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

