---
title: Propriedade canônica PidTagFreeBusyRangeTimestamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6c7dbbaf9d3d8cc09eef8a6ac193e786092bb8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571448"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="ec0da-103">Propriedade canônica PidTagFreeBusyRangeTimestamp</span><span class="sxs-lookup"><span data-stu-id="ec0da-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="ec0da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec0da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec0da-105">Contém a hora quando os dados foi publicados.</span><span class="sxs-lookup"><span data-stu-id="ec0da-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec0da-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ec0da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec0da-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="ec0da-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="ec0da-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ec0da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec0da-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="ec0da-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="ec0da-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ec0da-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec0da-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ec0da-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ec0da-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ec0da-112">Area:</span></span>  <br/> |<span data-ttu-id="ec0da-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="ec0da-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec0da-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec0da-114">Remarks</span></span>

<span data-ttu-id="ec0da-115">Essa propriedade é o número de minutos desde a meia-noite, 1 de janeiro de 1601 no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="ec0da-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ec0da-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec0da-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec0da-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ec0da-117">Protocol specifications</span></span>

<span data-ttu-id="ec0da-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec0da-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec0da-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ec0da-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec0da-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec0da-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec0da-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="ec0da-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec0da-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec0da-122">Header files</span></span>

<span data-ttu-id="ec0da-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec0da-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec0da-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ec0da-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec0da-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec0da-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ec0da-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ec0da-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec0da-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec0da-127">See also</span></span>



[<span data-ttu-id="ec0da-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ec0da-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec0da-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ec0da-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec0da-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ec0da-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec0da-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ec0da-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

