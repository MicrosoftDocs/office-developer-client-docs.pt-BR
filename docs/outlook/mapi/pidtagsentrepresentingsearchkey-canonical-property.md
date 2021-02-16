---
title: Propriedade canônica PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356683"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="55c0e-103">Propriedade canônica PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="55c0e-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="55c0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55c0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55c0e-105">Contém a chave de pesquisa para o usuário de mensagens representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="55c0e-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55c0e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="55c0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55c0e-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="55c0e-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="55c0e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="55c0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55c0e-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="55c0e-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="55c0e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="55c0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="55c0e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="55c0e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="55c0e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="55c0e-112">Area:</span></span>  <br/> |<span data-ttu-id="55c0e-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="55c0e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c0e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c0e-114">Remarks</span></span>

<span data-ttu-id="55c0e-115">Essa propriedade é uma das propriedades de endereço do usuário de mensagens que está sendo representado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="55c0e-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="55c0e-116">Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades do remetente representado para os valores desse cliente.</span><span class="sxs-lookup"><span data-stu-id="55c0e-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="55c0e-117">Um usuário de mensagens que envia em seu próprio nome normalmente deixa as propriedades do remetente representadas desaperadas.</span><span class="sxs-lookup"><span data-stu-id="55c0e-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="55c0e-118">O provedor de transporte de saída deve sempre deixar essa propriedade inalterada se tiver sido definida pelo cliente de envio.</span><span class="sxs-lookup"><span data-stu-id="55c0e-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="55c0e-119">Se não for definido, o provedor de transporte deverá defini-la como **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) na cópia de saída da mensagem e deixá-la desa definida na cópia local.</span><span class="sxs-lookup"><span data-stu-id="55c0e-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55c0e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55c0e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55c0e-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="55c0e-121">Protocol specifications</span></span>

<span data-ttu-id="55c0e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-123">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="55c0e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55c0e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-125">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="55c0e-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="55c0e-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-127">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="55c0e-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="55c0e-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-129">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="55c0e-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="55c0e-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-131">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="55c0e-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="55c0e-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-133">Especifica as propriedades e operações que são permitidas para postagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="55c0e-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="55c0e-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c0e-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c0e-135">Especifica as propriedades e operações que são permitidas para listas de contatos e distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="55c0e-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55c0e-136">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="55c0e-136">Header files</span></span>

<span data-ttu-id="55c0e-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55c0e-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="55c0e-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="55c0e-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="55c0e-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55c0e-139">Mapitags.h</span></span>
  
> <span data-ttu-id="55c0e-140">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="55c0e-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55c0e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c0e-141">See also</span></span>



[<span data-ttu-id="55c0e-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55c0e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55c0e-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="55c0e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55c0e-144">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="55c0e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55c0e-145">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="55c0e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

