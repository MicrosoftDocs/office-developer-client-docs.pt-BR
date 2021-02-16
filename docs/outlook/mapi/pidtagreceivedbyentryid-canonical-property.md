---
title: Propriedade canônica PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2f0203fc787ced9a0198be10c238f6245cb15144
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359217"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="5b45e-103">Propriedade canônica PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="5b45e-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5b45e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b45e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b45e-105">Contém o identificador de entrada do usuário de mensagens que realmente recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b45e-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b45e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5b45e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b45e-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5b45e-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5b45e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5b45e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b45e-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="5b45e-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="5b45e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5b45e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b45e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5b45e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5b45e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5b45e-112">Area:</span></span>  <br/> |<span data-ttu-id="5b45e-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5b45e-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b45e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b45e-114">Remarks</span></span>

<span data-ttu-id="5b45e-115">Essa propriedade é uma das propriedades de endereço do usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b45e-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="5b45e-116">Ele deve ser definido pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b45e-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="5b45e-117">Essa propriedade corresponde a um envelope de entrega X.400 por MH_T_ mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b45e-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b45e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b45e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b45e-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5b45e-119">Protocol specifications</span></span>

<span data-ttu-id="5b45e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b45e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b45e-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5b45e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b45e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b45e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b45e-123">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="5b45e-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5b45e-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b45e-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b45e-125">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="5b45e-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5b45e-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b45e-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b45e-127">Converte entre IETF RFC2445, RFC2446 e RFC2447 e itens de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="5b45e-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="5b45e-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b45e-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b45e-129">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="5b45e-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="5b45e-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b45e-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b45e-131">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5b45e-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b45e-132">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="5b45e-132">Header files</span></span>

<span data-ttu-id="5b45e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b45e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b45e-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5b45e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b45e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b45e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5b45e-136">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="5b45e-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b45e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b45e-137">See also</span></span>



[<span data-ttu-id="5b45e-138">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="5b45e-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="5b45e-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b45e-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b45e-140">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5b45e-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b45e-141">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b45e-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b45e-142">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5b45e-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

