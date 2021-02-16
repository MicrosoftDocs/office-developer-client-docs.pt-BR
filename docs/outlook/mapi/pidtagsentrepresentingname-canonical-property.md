---
title: Propriedade canônica PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314928"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="3e700-103">Propriedade canônica PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="3e700-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="3e700-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e700-105">Contém o nome para exibição do usuário de mensagens representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="3e700-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e700-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3e700-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e700-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3e700-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3e700-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3e700-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e700-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="3e700-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="3e700-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3e700-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e700-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3e700-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3e700-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3e700-112">Area:</span></span>  <br/> |<span data-ttu-id="3e700-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="3e700-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e700-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e700-114">Remarks</span></span>

<span data-ttu-id="3e700-115">Essas propriedades são exemplos das propriedades de endereço do usuário de mensagens que está sendo representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="3e700-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="3e700-116">Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades do remetente representado para os valores desse cliente.</span><span class="sxs-lookup"><span data-stu-id="3e700-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="3e700-117">Um usuário de mensagens que envia em seu próprio nome normalmente deixa as propriedades do remetente representadas desaperadas.</span><span class="sxs-lookup"><span data-stu-id="3e700-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="3e700-118">O provedor de transporte de saída deve sempre deixar essa propriedade inalterada se tiver sido definida pelo cliente de envio.</span><span class="sxs-lookup"><span data-stu-id="3e700-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="3e700-119">Se não estiver definido, o provedor de transporte deverá defini-lo como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) na cópia de saída da mensagem e deixá-la sem definição na cópia local.</span><span class="sxs-lookup"><span data-stu-id="3e700-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3e700-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e700-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e700-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3e700-121">Protocol specifications</span></span>

<span data-ttu-id="3e700-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-123">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3e700-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e700-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-125">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="3e700-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="3e700-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-127">Especifica as propriedades e operações que representam itens RSS.</span><span class="sxs-lookup"><span data-stu-id="3e700-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="3e700-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-129">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="3e700-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3e700-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-131">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="3e700-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="3e700-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-133">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3e700-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="3e700-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-135">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="3e700-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="3e700-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-137">Especifica o local e as propriedades dos dados de configuração do cliente e do servidor, como listas de categorias compartilhadas e horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3e700-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="3e700-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-139">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="3e700-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="3e700-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-141">Especifica as propriedades e operações que são permitidas para postagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="3e700-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="3e700-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-143">Especifica as propriedades e operações que são permitidas para contatos e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="3e700-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="3e700-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e700-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e700-145">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3e700-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e700-146">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3e700-146">Header files</span></span>

<span data-ttu-id="3e700-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e700-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e700-148">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e700-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e700-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3e700-149">Mapitags.h</span></span>
  
> <span data-ttu-id="3e700-150">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="3e700-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e700-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e700-151">See also</span></span>



[<span data-ttu-id="3e700-152">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="3e700-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="3e700-153">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e700-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e700-154">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3e700-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e700-155">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3e700-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e700-156">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3e700-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

