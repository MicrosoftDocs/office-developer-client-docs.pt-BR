---
title: Propriedade canônica PidTagTransportMessageHeaders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e184fd0933295984af97258d785df92306160a6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770170"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="e5f6a-103">Propriedade canônica PidTagTransportMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="e5f6a-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="e5f6a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5f6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5f6a-105">Contém informações de envelope de mensagem específicos de transporte.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5f6a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e5f6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5f6a-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="e5f6a-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="e5f6a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e5f6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5f6a-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="e5f6a-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="e5f6a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e5f6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5f6a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5f6a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e5f6a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e5f6a-112">Area:</span></span>  <br/> |<span data-ttu-id="e5f6a-113">Email</span><span class="sxs-lookup"><span data-stu-id="e5f6a-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5f6a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5f6a-114">Remarks</span></span>

<span data-ttu-id="e5f6a-115">O provedor de transporte pode gerar informações de cabeçalho da mensagem para mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="e5f6a-116">Essas propriedades oferecem uma alternativa para descartar as informações de cabeçalho de mensagem de transporte ou anexando ao início para o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="e5f6a-117">O cliente pode escolher se deseja ou não exibir as informações.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5f6a-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5f6a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5f6a-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e5f6a-119">Protocol specifications</span></span>

<span data-ttu-id="e5f6a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5f6a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5f6a-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5f6a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5f6a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5f6a-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="e5f6a-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5f6a-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5f6a-125">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5f6a-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e5f6a-126">Header files</span></span>

<span data-ttu-id="e5f6a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5f6a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5f6a-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5f6a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5f6a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e5f6a-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e5f6a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5f6a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5f6a-131">See also</span></span>



[<span data-ttu-id="e5f6a-132">Propriedade canônica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="e5f6a-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="e5f6a-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e5f6a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5f6a-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e5f6a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5f6a-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e5f6a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5f6a-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e5f6a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
