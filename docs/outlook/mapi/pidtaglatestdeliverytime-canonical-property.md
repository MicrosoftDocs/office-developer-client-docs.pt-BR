---
title: Propriedade canônica PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407785"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="84169-103">Propriedade canônica PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="84169-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="84169-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84169-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84169-105">Contém a data e a hora mais recentes em que um MTA (agente de transferência de mensagens) deve entregar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="84169-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84169-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="84169-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84169-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="84169-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="84169-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="84169-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84169-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="84169-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="84169-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="84169-110">Data type:</span></span>  <br/> |<span data-ttu-id="84169-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="84169-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="84169-112">Área:</span><span class="sxs-lookup"><span data-stu-id="84169-112">Area:</span></span>  <br/> |<span data-ttu-id="84169-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="84169-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84169-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="84169-114">Remarks</span></span>

<span data-ttu-id="84169-115">Se um MTA não puder entregar uma mensagem até o momento especificado por essa propriedade, ele cancelará a mensagem sem entrega.</span><span class="sxs-lookup"><span data-stu-id="84169-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="84169-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="84169-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="84169-117">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="84169-117">Header files</span></span>

<span data-ttu-id="84169-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84169-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="84169-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="84169-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="84169-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84169-120">Mapitags.h</span></span>
  
> <span data-ttu-id="84169-121">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="84169-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84169-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="84169-122">See also</span></span>



[<span data-ttu-id="84169-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="84169-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84169-124">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="84169-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84169-125">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="84169-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84169-126">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="84169-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

