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
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="1dfbb-103">Propriedade canônica PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="1dfbb-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="1dfbb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dfbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dfbb-105">Contém a hora de término do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1dfbb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1dfbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1dfbb-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="1dfbb-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="1dfbb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1dfbb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1dfbb-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="1dfbb-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="1dfbb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1dfbb-110">Data type:</span></span>  <br/> |<span data-ttu-id="1dfbb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1dfbb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1dfbb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1dfbb-112">Area:</span></span>  <br/> |<span data-ttu-id="1dfbb-113">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1dfbb-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dfbb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dfbb-114">Remarks</span></span>

<span data-ttu-id="1dfbb-115">O valor dessa propriedade é calculado adicionando-se o valor de **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) à data de início do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="1dfbb-116">Esse valor é expresso como o número de minutos desde a meia-noite, 1º de janeiro de 1601 em tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="1dfbb-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1dfbb-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dfbb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1dfbb-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="1dfbb-118">Protocol specifications</span></span>

<span data-ttu-id="1dfbb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dfbb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dfbb-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1dfbb-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dfbb-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dfbb-122">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1dfbb-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1dfbb-123">Header files</span></span>

<span data-ttu-id="1dfbb-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1dfbb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1dfbb-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1dfbb-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1dfbb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1dfbb-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1dfbb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dfbb-128">See also</span></span>



[<span data-ttu-id="1dfbb-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1dfbb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1dfbb-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1dfbb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1dfbb-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1dfbb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1dfbb-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1dfbb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

