---
title: Propriedade canônica PidTagReceivedByName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByName
api_type:
- COM
ms.assetid: edd29217-74bb-4321-82fd-65f0fbfd05f8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 039a51c2bb4cf1fe2a83e2ba144a87462b5d6d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359210"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="557b4-103">Propriedade canônica PidTagReceivedByName</span><span class="sxs-lookup"><span data-stu-id="557b4-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="557b4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="557b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="557b4-105">Contém o nome de exibição do usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="557b4-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="557b4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="557b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="557b4-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="557b4-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="557b4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="557b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="557b4-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="557b4-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="557b4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="557b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="557b4-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="557b4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="557b4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="557b4-112">Area:</span></span>  <br/> |<span data-ttu-id="557b4-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="557b4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="557b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="557b4-114">Remarks</span></span>

<span data-ttu-id="557b4-115">Essas propriedades são um exemplo das propriedades de endereço do usuário que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="557b4-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="557b4-116">Eles devem ser definidos pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="557b4-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="557b4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="557b4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="557b4-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="557b4-118">Protocol specifications</span></span>

<span data-ttu-id="557b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="557b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="557b4-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="557b4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="557b4-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="557b4-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="557b4-122">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="557b4-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="557b4-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="557b4-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="557b4-124">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="557b4-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="557b4-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="557b4-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="557b4-126">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="557b4-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="557b4-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="557b4-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="557b4-128">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="557b4-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="557b4-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="557b4-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="557b4-130">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="557b4-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="557b4-131">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="557b4-131">Header files</span></span>

<span data-ttu-id="557b4-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="557b4-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="557b4-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="557b4-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="557b4-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="557b4-134">Mapitags.h</span></span>
  
> <span data-ttu-id="557b4-135">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="557b4-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="557b4-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="557b4-136">See also</span></span>



[<span data-ttu-id="557b4-137">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="557b4-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="557b4-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="557b4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="557b4-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="557b4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="557b4-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="557b4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="557b4-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="557b4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

