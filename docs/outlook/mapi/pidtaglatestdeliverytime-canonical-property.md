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
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590922"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="039d0-103">Propriedade canônica PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="039d0-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="039d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="039d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="039d0-105">Contém a última data e hora quando um agente de transferência de mensagem (MTA) deve proporcionar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="039d0-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="039d0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="039d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="039d0-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="039d0-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="039d0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="039d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="039d0-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="039d0-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="039d0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="039d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="039d0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="039d0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="039d0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="039d0-112">Area:</span></span>  <br/> |<span data-ttu-id="039d0-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="039d0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="039d0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="039d0-114">Remarks</span></span>

<span data-ttu-id="039d0-115">Se um MTA não pode enviar uma mensagem no momento em que esta propriedade especifica, ele cancela a mensagem sem entrega.</span><span class="sxs-lookup"><span data-stu-id="039d0-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="039d0-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="039d0-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="039d0-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="039d0-117">Header files</span></span>

<span data-ttu-id="039d0-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="039d0-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="039d0-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="039d0-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="039d0-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="039d0-120">Mapitags.h</span></span>
  
> <span data-ttu-id="039d0-121">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="039d0-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="039d0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="039d0-122">See also</span></span>



[<span data-ttu-id="039d0-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="039d0-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="039d0-124">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="039d0-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="039d0-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="039d0-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="039d0-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="039d0-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

