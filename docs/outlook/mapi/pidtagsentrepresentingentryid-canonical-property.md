---
title: Propriedade canônica PidTagSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385491"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="469a2-103">Propriedade canônica PidTagSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="469a2-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="469a2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="469a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="469a2-105">Contém o identificador de entrada para o usuário mensagens representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="469a2-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="469a2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="469a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="469a2-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="469a2-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="469a2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="469a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="469a2-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="469a2-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="469a2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="469a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="469a2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="469a2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="469a2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="469a2-112">Area:</span></span>  <br/> |<span data-ttu-id="469a2-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="469a2-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="469a2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="469a2-114">Remarks</span></span>

<span data-ttu-id="469a2-115">Essa propriedade é uma das propriedades de endereço para o usuário de mensagens está sendo representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="469a2-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="469a2-116">Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades de remetente representado para os valores para que o cliente.</span><span class="sxs-lookup"><span data-stu-id="469a2-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="469a2-117">Um usuário de mensagens enviando em seu próprio nome geralmente deixa as propriedades de remetente representado não definidas.</span><span class="sxs-lookup"><span data-stu-id="469a2-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="469a2-118">O provedor de transporte de saída deve sempre deixar essa propriedade inalterada se ele tiver sido definido pelo cliente de envio.</span><span class="sxs-lookup"><span data-stu-id="469a2-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="469a2-119">Se ela foi removida, o provedor de transporte deve defini-la como **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) na cópia de saída da mensagem e deixá-lo não definidas na cópia local.</span><span class="sxs-lookup"><span data-stu-id="469a2-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="469a2-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="469a2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="469a2-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="469a2-121">Protocol specifications</span></span>

<span data-ttu-id="469a2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="469a2-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="469a2-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-125">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="469a2-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="469a2-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-127">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="469a2-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="469a2-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-129">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="469a2-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="469a2-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-131">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="469a2-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="469a2-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-133">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="469a2-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="469a2-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="469a2-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="469a2-135">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="469a2-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="469a2-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="469a2-136">Header files</span></span>

<span data-ttu-id="469a2-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="469a2-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="469a2-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="469a2-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="469a2-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="469a2-139">Mapitags.h</span></span>
  
> <span data-ttu-id="469a2-140">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="469a2-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="469a2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="469a2-141">See also</span></span>



[<span data-ttu-id="469a2-142">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="469a2-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="469a2-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="469a2-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="469a2-144">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="469a2-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="469a2-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="469a2-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="469a2-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="469a2-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

