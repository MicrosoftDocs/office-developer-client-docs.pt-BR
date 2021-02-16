---
title: Propriedade canônica PidTagFreeBusyPublishEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b4a8cb7136eee914dc697d24e0374ccb4b6f8b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316181"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="9c467-103">Propriedade canônica PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="9c467-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="9c467-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c467-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c467-105">Contém a hora de término do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="9c467-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c467-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9c467-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c467-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="9c467-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="9c467-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9c467-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c467-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="9c467-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="9c467-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9c467-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c467-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9c467-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9c467-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9c467-112">Area:</span></span>  <br/> |<span data-ttu-id="9c467-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="9c467-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c467-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c467-114">Remarks</span></span>

<span data-ttu-id="9c467-115">O valor dessa propriedade é calculado adicionando-se o valor de **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) à data de início do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="9c467-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="9c467-116">Esse valor é expresso como o número de minutos desde a meia-noite de 1º de janeiro de 1601 no Tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="9c467-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c467-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c467-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9c467-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9c467-118">Protocol specifications</span></span>

<span data-ttu-id="9c467-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c467-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c467-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9c467-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9c467-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c467-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c467-122">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="9c467-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9c467-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9c467-123">Header files</span></span>

<span data-ttu-id="9c467-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c467-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c467-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9c467-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c467-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9c467-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9c467-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9c467-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c467-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c467-128">See also</span></span>



[<span data-ttu-id="9c467-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9c467-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c467-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9c467-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c467-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9c467-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c467-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9c467-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

