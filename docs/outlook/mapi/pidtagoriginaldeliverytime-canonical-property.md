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
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355654"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="d325c-103">Propriedade canônica PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="d325c-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="d325c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d325c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d325c-105">Contém uma cópia da data e hora de entrega da mensagem original em um thread.</span><span class="sxs-lookup"><span data-stu-id="d325c-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d325c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d325c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d325c-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="d325c-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="d325c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d325c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d325c-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="d325c-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="d325c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d325c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d325c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d325c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d325c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d325c-112">Area:</span></span>  <br/> |<span data-ttu-id="d325c-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="d325c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d325c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d325c-114">Remarks</span></span>

<span data-ttu-id="d325c-115">Essa propriedade é copiada da propriedade original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) em operações subsequentes de resposta ou encaminhamento e usada em relatórios lidos e não lidos.</span><span class="sxs-lookup"><span data-stu-id="d325c-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="d325c-116">Relatórios de entrega usam a **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d325c-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d325c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d325c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d325c-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d325c-118">Protocol specifications</span></span>

<span data-ttu-id="d325c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d325c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d325c-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d325c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d325c-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d325c-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d325c-122">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d325c-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d325c-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d325c-123">Header files</span></span>

<span data-ttu-id="d325c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d325c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d325c-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d325c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d325c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d325c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d325c-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d325c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d325c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d325c-128">See also</span></span>



[<span data-ttu-id="d325c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d325c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d325c-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d325c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d325c-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d325c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d325c-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d325c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

