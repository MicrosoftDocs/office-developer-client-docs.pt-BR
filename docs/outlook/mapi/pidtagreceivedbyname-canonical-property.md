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
ms.openlocfilehash: 7b564b1dda1d72a28e16fad40f0ef90451aaaf0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769746"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="115d0-103">Propriedade canônica PidTagReceivedByName</span><span class="sxs-lookup"><span data-stu-id="115d0-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="115d0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="115d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="115d0-105">Contém o nome de exibição do usuário mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="115d0-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="115d0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="115d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="115d0-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="115d0-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="115d0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="115d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="115d0-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="115d0-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="115d0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="115d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="115d0-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="115d0-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="115d0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="115d0-112">Area:</span></span>  <br/> |<span data-ttu-id="115d0-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="115d0-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="115d0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="115d0-114">Remarks</span></span>

<span data-ttu-id="115d0-115">Essas propriedades são um exemplo das propriedades de endereço para o usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="115d0-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="115d0-116">Devem ser definidas pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="115d0-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="115d0-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="115d0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="115d0-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="115d0-118">Protocol specifications</span></span>

<span data-ttu-id="115d0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115d0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115d0-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="115d0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="115d0-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115d0-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115d0-122">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="115d0-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="115d0-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115d0-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115d0-124">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="115d0-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="115d0-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115d0-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115d0-126">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="115d0-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="115d0-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115d0-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115d0-128">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="115d0-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="115d0-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115d0-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115d0-130">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="115d0-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="115d0-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="115d0-131">Header files</span></span>

<span data-ttu-id="115d0-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="115d0-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="115d0-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="115d0-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="115d0-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="115d0-134">Mapitags.h</span></span>
  
> <span data-ttu-id="115d0-135">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="115d0-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="115d0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="115d0-136">See also</span></span>



[<span data-ttu-id="115d0-137">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="115d0-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="115d0-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="115d0-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="115d0-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="115d0-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="115d0-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="115d0-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="115d0-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="115d0-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
