---
title: Propriedade canônica PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 30ee7c1a7eb86fd4cdfe90fb6711bd1b295fd5e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591083"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="7fdde-103">Propriedade canônica PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="7fdde-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="7fdde-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fdde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fdde-105">Contém um número que pode ser usado para calcular a adiar a necessidade de enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7fdde-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fdde-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7fdde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fdde-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="7fdde-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="7fdde-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7fdde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7fdde-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="7fdde-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="7fdde-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7fdde-110">Data type:</span></span>  <br/> |<span data-ttu-id="7fdde-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7fdde-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7fdde-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7fdde-112">Area:</span></span>  <br/> |<span data-ttu-id="7fdde-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="7fdde-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fdde-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fdde-114">Remarks</span></span>

<span data-ttu-id="7fdde-115">Essa propriedade é usada para computação a propriedade **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) quando não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="7fdde-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="7fdde-116">Ao enviar uma mensagem é adiada, a propriedade **PR_DEFERRED_SEND_NUMBER** deve ser definida juntamente com a propriedade **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), se a propriedade **PR_DEFERRED_SEND_TIME** não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="7fdde-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="7fdde-117">O valor **PR_DEFERRED_SEND_NUMBER** deve ser definido entre 0 e 999.</span><span class="sxs-lookup"><span data-stu-id="7fdde-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7fdde-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fdde-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fdde-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7fdde-119">Protocol specifications</span></span>

<span data-ttu-id="7fdde-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fdde-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fdde-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="7fdde-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fdde-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7fdde-122">Header files</span></span>

<span data-ttu-id="7fdde-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fdde-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fdde-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7fdde-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7fdde-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7fdde-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7fdde-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7fdde-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fdde-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fdde-127">See also</span></span>



[<span data-ttu-id="7fdde-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7fdde-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fdde-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7fdde-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fdde-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7fdde-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fdde-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7fdde-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

