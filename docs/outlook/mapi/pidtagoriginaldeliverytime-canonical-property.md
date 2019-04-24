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
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="0e6b2-103">Propriedade canônica PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="0e6b2-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="0e6b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e6b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e6b2-105">Contém uma cópia da data e hora de entrega da mensagem original em um thread.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e6b2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0e6b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e6b2-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="0e6b2-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="0e6b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e6b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e6b2-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="0e6b2-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="0e6b2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0e6b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e6b2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0e6b2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0e6b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0e6b2-112">Area:</span></span>  <br/> |<span data-ttu-id="0e6b2-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="0e6b2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e6b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e6b2-114">Remarks</span></span>

<span data-ttu-id="0e6b2-115">Essa propriedade é copiada da **PR_MESSAGE_DELIVERY_TIME** original ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) em operações de resposta ou encaminhamento subsequentes e usada nos relatórios de leitura e não leitura.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="0e6b2-116">Os relatórios de entrega usam a propriedade **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e6b2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e6b2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e6b2-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="0e6b2-118">Protocol specifications</span></span>

<span data-ttu-id="0e6b2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e6b2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e6b2-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e6b2-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e6b2-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e6b2-122">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e6b2-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e6b2-123">Header files</span></span>

<span data-ttu-id="0e6b2-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0e6b2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e6b2-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e6b2-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0e6b2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="0e6b2-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0e6b2-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e6b2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e6b2-128">See also</span></span>



[<span data-ttu-id="0e6b2-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6b2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e6b2-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6b2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e6b2-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6b2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e6b2-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0e6b2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

