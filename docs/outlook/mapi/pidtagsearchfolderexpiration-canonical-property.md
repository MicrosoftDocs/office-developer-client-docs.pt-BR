---
title: Propriedade canônica PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336467"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="bc889-103">Propriedade canônica PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="bc889-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="bc889-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc889-105">Contém a hora em que o contêiner da pasta de pesquisa ficará e deve ser atualizado ou recriado.</span><span class="sxs-lookup"><span data-stu-id="bc889-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc889-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bc889-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc889-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="bc889-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="bc889-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bc889-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc889-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="bc889-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="bc889-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bc889-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc889-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bc889-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bc889-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bc889-112">Area:</span></span>  <br/> |<span data-ttu-id="bc889-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="bc889-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc889-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc889-114">Remarks</span></span>

<span data-ttu-id="bc889-115">Essa propriedade deve ser formatada como o número de minutos desde a meia-noite em UTC (Tempo Universal Coordenado) de 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="bc889-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc889-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc889-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc889-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bc889-117">Protocol specifications</span></span>

<span data-ttu-id="bc889-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc889-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc889-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bc889-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc889-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc889-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc889-121">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bc889-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc889-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="bc889-122">Header files</span></span>

<span data-ttu-id="bc889-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc889-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc889-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bc889-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc889-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc889-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bc889-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bc889-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc889-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc889-127">See also</span></span>



[<span data-ttu-id="bc889-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bc889-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc889-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bc889-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc889-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bc889-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc889-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bc889-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

