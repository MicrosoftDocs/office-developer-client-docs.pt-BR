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
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769425"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="973b2-103">Propriedade canônica PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="973b2-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="973b2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="973b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="973b2-105">Contém a última data e hora quando um agente de transferência de mensagem (MTA) deve proporcionar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="973b2-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="973b2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="973b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="973b2-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="973b2-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="973b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="973b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="973b2-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="973b2-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="973b2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="973b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="973b2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="973b2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="973b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="973b2-112">Area:</span></span>  <br/> |<span data-ttu-id="973b2-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="973b2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="973b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="973b2-114">Remarks</span></span>

<span data-ttu-id="973b2-115">Se um MTA não pode enviar uma mensagem no momento em que esta propriedade especifica, ele cancela a mensagem sem entrega.</span><span class="sxs-lookup"><span data-stu-id="973b2-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="973b2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="973b2-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="973b2-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="973b2-117">Header files</span></span>

<span data-ttu-id="973b2-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="973b2-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="973b2-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="973b2-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="973b2-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="973b2-120">Mapitags.h</span></span>
  
> <span data-ttu-id="973b2-121">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="973b2-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="973b2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="973b2-122">See also</span></span>



[<span data-ttu-id="973b2-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="973b2-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="973b2-124">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="973b2-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="973b2-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="973b2-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="973b2-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="973b2-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

