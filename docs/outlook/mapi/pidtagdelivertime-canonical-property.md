---
title: Propriedade canônica PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 40839e34a61b5e5fdd3d7b69d8c553d7e469cd22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769167"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="a248b-103">Propriedade canônica PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="a248b-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="a248b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a248b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a248b-105">Contém a data e hora de quando a mensagem original foi entregue.</span><span class="sxs-lookup"><span data-stu-id="a248b-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a248b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a248b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a248b-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="a248b-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="a248b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a248b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a248b-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="a248b-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="a248b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a248b-110">Data type:</span></span>  <br/> |<span data-ttu-id="a248b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a248b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a248b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a248b-112">Area:</span></span>  <br/> |<span data-ttu-id="a248b-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="a248b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a248b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a248b-114">Remarks</span></span>

<span data-ttu-id="a248b-115">Essa propriedade é uma propriedade por destinatário em um relatório de entrega que indica a hora em que a mensagem original foi entregue ao usuário mensagens para o qual o relatório de entrega está sendo gerado.</span><span class="sxs-lookup"><span data-stu-id="a248b-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a248b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a248b-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a248b-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a248b-117">Header files</span></span>

<span data-ttu-id="a248b-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a248b-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="a248b-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a248b-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="a248b-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a248b-120">Mapitags.h</span></span>
  
> <span data-ttu-id="a248b-121">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a248b-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a248b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a248b-122">See also</span></span>



[<span data-ttu-id="a248b-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="a248b-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="a248b-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a248b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a248b-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a248b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a248b-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a248b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a248b-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a248b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

