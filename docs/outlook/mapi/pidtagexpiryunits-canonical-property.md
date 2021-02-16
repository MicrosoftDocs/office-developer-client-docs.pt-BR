---
title: Propriedade canônica PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316405"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="b6da7-103">Propriedade canônica PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="b6da7-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="b6da7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6da7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6da7-105">Descreve a unidade de tempo quando a **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) se multiplica.</span><span class="sxs-lookup"><span data-stu-id="b6da7-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6da7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b6da7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6da7-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="b6da7-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="b6da7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b6da7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6da7-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="b6da7-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="b6da7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b6da7-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6da7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b6da7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b6da7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b6da7-112">Area:</span></span>  <br/> |<span data-ttu-id="b6da7-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="b6da7-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6da7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6da7-114">Remarks</span></span>

<span data-ttu-id="b6da7-115">Essa propriedade, se definida, deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b6da7-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6da7-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="b6da7-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="b6da7-117">Description (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="b6da7-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="b6da7-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6da7-118">0x00000000</span></span>  <br/> |<span data-ttu-id="b6da7-119">Minutos, por exemplo, 60 segundos</span><span class="sxs-lookup"><span data-stu-id="b6da7-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="b6da7-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b6da7-120">0x00000001</span></span>  <br/> |<span data-ttu-id="b6da7-121">Horas, por exemplo, 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="b6da7-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b6da7-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b6da7-122">0x00000002</span></span>  <br/> |<span data-ttu-id="b6da7-123">Day, for example 24x60x60 seconds</span><span class="sxs-lookup"><span data-stu-id="b6da7-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b6da7-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b6da7-124">0x00000003</span></span>  <br/> |<span data-ttu-id="b6da7-125">Semana, por exemplo, 7x24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="b6da7-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b6da7-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6da7-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6da7-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b6da7-127">Protocol specifications</span></span>

<span data-ttu-id="b6da7-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6da7-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6da7-129">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b6da7-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6da7-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b6da7-130">Header files</span></span>

<span data-ttu-id="b6da7-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6da7-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6da7-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b6da7-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6da7-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6da7-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b6da7-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b6da7-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6da7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6da7-135">See also</span></span>



[<span data-ttu-id="b6da7-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b6da7-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6da7-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b6da7-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6da7-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b6da7-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6da7-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b6da7-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

