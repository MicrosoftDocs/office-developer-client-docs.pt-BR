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
ms.openlocfilehash: 16c3684176de765a10b5bac620ea65a824cfe83a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588759"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="d7945-103">Propriedade canônica PidTagTransportMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="d7945-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="d7945-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7945-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7945-105">Contém informações de envelope de mensagem específicos de transporte.</span><span class="sxs-lookup"><span data-stu-id="d7945-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7945-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d7945-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7945-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="d7945-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="d7945-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7945-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7945-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="d7945-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="d7945-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d7945-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7945-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d7945-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d7945-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7945-112">Area:</span></span>  <br/> |<span data-ttu-id="d7945-113">Email</span><span class="sxs-lookup"><span data-stu-id="d7945-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7945-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7945-114">Remarks</span></span>

<span data-ttu-id="d7945-115">O provedor de transporte pode gerar informações de cabeçalho da mensagem para mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7945-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="d7945-116">Essas propriedades oferecem uma alternativa para descartar as informações de cabeçalho de mensagem de transporte ou anexando ao início para o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7945-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="d7945-117">O cliente pode escolher se deseja ou não exibir as informações.</span><span class="sxs-lookup"><span data-stu-id="d7945-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7945-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7945-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7945-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d7945-119">Protocol specifications</span></span>

<span data-ttu-id="d7945-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7945-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7945-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d7945-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7945-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7945-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7945-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d7945-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="d7945-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7945-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7945-125">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7945-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7945-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d7945-126">Header files</span></span>

<span data-ttu-id="d7945-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7945-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7945-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d7945-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7945-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7945-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d7945-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d7945-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7945-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7945-131">See also</span></span>



[<span data-ttu-id="d7945-132">Propriedade canônica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="d7945-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="d7945-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7945-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7945-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d7945-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7945-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d7945-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7945-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d7945-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

