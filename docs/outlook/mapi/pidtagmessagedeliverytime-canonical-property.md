---
title: Propriedade canônica PidTagMessageDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b635ad72acc2bd98ca0c207dea71ea2df757e22b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593932"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="3a77b-103">Propriedade canônica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="3a77b-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="3a77b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a77b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a77b-105">Contém a data e hora quando uma mensagem foi entregue.</span><span class="sxs-lookup"><span data-stu-id="3a77b-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a77b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3a77b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a77b-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="3a77b-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="3a77b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3a77b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3a77b-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="3a77b-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="3a77b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3a77b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3a77b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3a77b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3a77b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3a77b-112">Area:</span></span>  <br/> |<span data-ttu-id="3a77b-113">Hora da mensagem</span><span class="sxs-lookup"><span data-stu-id="3a77b-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a77b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a77b-114">Remarks</span></span>

<span data-ttu-id="3a77b-115">Essa propriedade descreve o tempo que a mensagem foi armazenada no servidor, ao invés do tempo de download quando o provedor de transporte copiado a mensagem do servidor para o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="3a77b-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a77b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a77b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a77b-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3a77b-117">Protocol specifications</span></span>

<span data-ttu-id="3a77b-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a77b-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a77b-119">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="3a77b-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a77b-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a77b-120">Header files</span></span>

<span data-ttu-id="3a77b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a77b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a77b-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3a77b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="3a77b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3a77b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="3a77b-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3a77b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a77b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a77b-125">See also</span></span>



[<span data-ttu-id="3a77b-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3a77b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a77b-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3a77b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a77b-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3a77b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a77b-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3a77b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

