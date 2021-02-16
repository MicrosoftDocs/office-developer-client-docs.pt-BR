---
title: Propriedade canônica PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316188"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="ec6df-103">Propriedade canônica PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="ec6df-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="ec6df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec6df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec6df-105">Contém o valor para calcular as datas de início e término do intervalo de dados de livre/ocupado a serem publicados em pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="ec6df-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec6df-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ec6df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec6df-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="ec6df-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="ec6df-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ec6df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec6df-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="ec6df-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="ec6df-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ec6df-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec6df-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ec6df-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ec6df-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ec6df-112">Area:</span></span>  <br/> |<span data-ttu-id="ec6df-113">Message class-defined transmitable</span><span class="sxs-lookup"><span data-stu-id="ec6df-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec6df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec6df-114">Remarks</span></span>

<span data-ttu-id="ec6df-115">O valor dessa propriedade deve ser maior ou igual a 0 e menor ou igual a 36.</span><span class="sxs-lookup"><span data-stu-id="ec6df-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="ec6df-116">Esta não é uma propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="ec6df-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ec6df-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec6df-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec6df-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ec6df-118">Protocol specifications</span></span>

<span data-ttu-id="ec6df-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec6df-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec6df-120">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="ec6df-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="ec6df-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec6df-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec6df-122">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="ec6df-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec6df-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ec6df-123">Header files</span></span>

<span data-ttu-id="ec6df-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec6df-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec6df-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ec6df-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec6df-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec6df-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ec6df-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ec6df-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec6df-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec6df-128">See also</span></span>



[<span data-ttu-id="ec6df-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6df-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec6df-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6df-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec6df-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6df-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec6df-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ec6df-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

