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
ms.openlocfilehash: 5417b73fe13937a74bc01520a2dd9db359e894ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770026"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="8e823-103">Propriedade canônica PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="8e823-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="8e823-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e823-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e823-105">Contém o nome de exibição para o usuário mensagens representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="8e823-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e823-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8e823-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e823-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8e823-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8e823-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8e823-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e823-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="8e823-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="8e823-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8e823-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e823-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8e823-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8e823-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8e823-112">Area:</span></span>  <br/> |<span data-ttu-id="8e823-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="8e823-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e823-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e823-114">Remarks</span></span>

<span data-ttu-id="8e823-115">Essas propriedades são exemplos das propriedades de endereço para o usuário de mensagens está sendo representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="8e823-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="8e823-116">Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades de remetente representado para os valores para que o cliente.</span><span class="sxs-lookup"><span data-stu-id="8e823-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="8e823-117">Um usuário de mensagens enviando em seu próprio nome geralmente deixa as propriedades de remetente representado não definidas.</span><span class="sxs-lookup"><span data-stu-id="8e823-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="8e823-118">O provedor de transporte de saída deve sempre deixar essa propriedade inalterada se ele tiver sido definido pelo cliente de envio.</span><span class="sxs-lookup"><span data-stu-id="8e823-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="8e823-119">Se ela foi removida, o provedor de transporte deve defini-la como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) na cópia de saída da mensagem e deixá-lo não definidas na cópia local.</span><span class="sxs-lookup"><span data-stu-id="8e823-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e823-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e823-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e823-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8e823-121">Protocol specifications</span></span>

<span data-ttu-id="8e823-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8e823-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e823-124">[[MS-OXOMSG]](http://msdn.microsoft.com/en-us/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-124">[[MS-OXOMSG]](http://msdn.microsoft.com/en-us/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-125">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8e823-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8e823-126">[[MS-OXORSS]](http://msdn.microsoft.com/en-us/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-126">[[MS-OXORSS]](http://msdn.microsoft.com/en-us/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-127">Especifica as propriedades e operações que representam os itens RSS.</span><span class="sxs-lookup"><span data-stu-id="8e823-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="8e823-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-129">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="8e823-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8e823-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-131">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="8e823-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8e823-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-133">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e823-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8e823-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-135">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="8e823-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8e823-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-137">Especifica o local e as propriedades de dados de configuração de cliente e servidor, como listas de categoria compartilhada e o horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e823-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="8e823-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-139">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="8e823-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8e823-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-141">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="8e823-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8e823-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-143">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="8e823-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="8e823-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e823-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e823-145">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="8e823-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e823-146">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e823-146">Header files</span></span>

<span data-ttu-id="8e823-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e823-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e823-148">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8e823-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e823-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e823-149">Mapitags.h</span></span>
  
> <span data-ttu-id="8e823-150">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8e823-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e823-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e823-151">See also</span></span>



[<span data-ttu-id="8e823-152">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="8e823-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="8e823-153">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e823-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e823-154">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8e823-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e823-155">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e823-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e823-156">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8e823-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

