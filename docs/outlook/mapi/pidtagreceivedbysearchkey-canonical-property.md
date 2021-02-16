---
title: Propriedade canônica PidTagReceivedBySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedBySearchKey
api_type:
- COM
ms.assetid: 4b37555a-1d07-4f42-95e3-b8fa37ed0c3b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bace518784bf24807cfca09032a4f3912f4e98ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359203"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="0ac37-103">Propriedade canônica PidTagReceivedBySearchKey</span><span class="sxs-lookup"><span data-stu-id="0ac37-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0ac37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ac37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ac37-105">Contém a chave de pesquisa do usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ac37-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ac37-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0ac37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ac37-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="0ac37-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0ac37-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0ac37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ac37-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="0ac37-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="0ac37-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0ac37-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ac37-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac37-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0ac37-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0ac37-112">Area:</span></span>  <br/> |<span data-ttu-id="0ac37-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="0ac37-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ac37-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ac37-114">Remarks</span></span>

<span data-ttu-id="0ac37-115">Essa propriedade é uma das propriedades de endereço do usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ac37-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="0ac37-116">Ele deve ser definido pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ac37-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ac37-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ac37-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ac37-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0ac37-118">Protocol specifications</span></span>

<span data-ttu-id="0ac37-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ac37-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ac37-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0ac37-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ac37-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ac37-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ac37-122">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="0ac37-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0ac37-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ac37-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ac37-124">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="0ac37-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0ac37-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ac37-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ac37-126">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="0ac37-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0ac37-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ac37-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ac37-128">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="0ac37-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="0ac37-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ac37-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ac37-130">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0ac37-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ac37-131">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0ac37-131">Header files</span></span>

<span data-ttu-id="0ac37-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ac37-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ac37-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0ac37-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ac37-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ac37-134">Mapitags.h</span></span>
  
> <span data-ttu-id="0ac37-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0ac37-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ac37-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ac37-136">See also</span></span>



[<span data-ttu-id="0ac37-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0ac37-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ac37-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0ac37-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ac37-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0ac37-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ac37-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0ac37-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

