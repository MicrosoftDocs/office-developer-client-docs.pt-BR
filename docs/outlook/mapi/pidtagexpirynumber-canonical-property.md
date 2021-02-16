---
title: Propriedade canônica PidTagExpiryNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316363"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="8befb-103">Propriedade canônica PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="8befb-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="8befb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8befb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8befb-105">Define o tempo de envio expirado em conjunto com a **propriedade PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8befb-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8befb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8befb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8befb-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="8befb-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="8befb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8befb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8befb-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="8befb-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="8befb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8befb-110">Data type:</span></span>  <br/> |<span data-ttu-id="8befb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8befb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8befb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8befb-112">Area:</span></span>  <br/> |<span data-ttu-id="8befb-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="8befb-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8befb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8befb-114">Remarks</span></span>

<span data-ttu-id="8befb-115">O valor dessa propriedade deve ser definido entre 0 e 999, inclusive, se estiver presente.</span><span class="sxs-lookup"><span data-stu-id="8befb-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8befb-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8befb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8befb-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8befb-117">Protocol specifications</span></span>

<span data-ttu-id="8befb-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8befb-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8befb-119">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8befb-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8befb-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="8befb-120">Header files</span></span>

<span data-ttu-id="8befb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8befb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8befb-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8befb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8befb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8befb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8befb-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8befb-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8befb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8befb-125">See also</span></span>



[<span data-ttu-id="8befb-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8befb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8befb-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8befb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8befb-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8befb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8befb-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8befb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

