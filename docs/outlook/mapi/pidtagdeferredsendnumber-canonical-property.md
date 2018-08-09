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
ms.openlocfilehash: f2ccd004415bcbd42b56b1269fbdb4622ef1f8c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769191"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="daa8c-103">Propriedade canônica PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="daa8c-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="daa8c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="daa8c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="daa8c-105">Contém um número que pode ser usado para calcular a adiar a necessidade de enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="daa8c-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daa8c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="daa8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="daa8c-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="daa8c-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="daa8c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="daa8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="daa8c-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="daa8c-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="daa8c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="daa8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="daa8c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="daa8c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="daa8c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="daa8c-112">Area:</span></span>  <br/> |<span data-ttu-id="daa8c-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="daa8c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daa8c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="daa8c-114">Remarks</span></span>

<span data-ttu-id="daa8c-115">Essa propriedade é usada para computação a propriedade **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) quando não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="daa8c-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="daa8c-116">Ao enviar uma mensagem é adiada, a propriedade **PR_DEFERRED_SEND_NUMBER** deve ser definida juntamente com a propriedade **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), se a propriedade **PR_DEFERRED_SEND_TIME** não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="daa8c-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="daa8c-117">O valor **PR_DEFERRED_SEND_NUMBER** deve ser definido entre 0 e 999.</span><span class="sxs-lookup"><span data-stu-id="daa8c-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="daa8c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="daa8c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="daa8c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="daa8c-119">Protocol specifications</span></span>

<span data-ttu-id="daa8c-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daa8c-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daa8c-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="daa8c-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="daa8c-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="daa8c-122">Header files</span></span>

<span data-ttu-id="daa8c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="daa8c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="daa8c-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="daa8c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="daa8c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="daa8c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="daa8c-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="daa8c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="daa8c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="daa8c-127">See also</span></span>



[<span data-ttu-id="daa8c-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="daa8c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="daa8c-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="daa8c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="daa8c-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="daa8c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="daa8c-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="daa8c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

