---
title: Propriedade canônica PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cd8c44923e64fcea4464f758389db05bb6b7e374
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769545"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="cb3bb-103">Propriedade canônica PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="cb3bb-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="cb3bb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb3bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb3bb-105">Contém uma cópia da data de entrega e a hora em um segmento da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="cb3bb-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb3bb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cb3bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb3bb-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="cb3bb-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="cb3bb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb3bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb3bb-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="cb3bb-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="cb3bb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cb3bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb3bb-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="cb3bb-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="cb3bb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb3bb-112">Area:</span></span>  <br/> |<span data-ttu-id="cb3bb-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="cb3bb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb3bb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb3bb-114">Remarks</span></span>

<span data-ttu-id="cb3bb-115">Essa propriedade é copiada da propriedade **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) original em subsequente responder ou encaminhar operações e usada em relatórios de leitura e nonread.</span><span class="sxs-lookup"><span data-stu-id="cb3bb-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="cb3bb-116">Notificações de entrega usam a propriedade **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cb3bb-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb3bb-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb3bb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb3bb-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb3bb-118">Protocol specifications</span></span>

<span data-ttu-id="cb3bb-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb3bb-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb3bb-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cb3bb-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb3bb-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb3bb-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb3bb-122">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="cb3bb-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb3bb-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb3bb-123">Header files</span></span>

<span data-ttu-id="cb3bb-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb3bb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb3bb-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cb3bb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb3bb-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb3bb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cb3bb-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cb3bb-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb3bb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb3bb-128">See also</span></span>



[<span data-ttu-id="cb3bb-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb3bb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb3bb-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cb3bb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb3bb-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cb3bb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb3bb-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cb3bb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

