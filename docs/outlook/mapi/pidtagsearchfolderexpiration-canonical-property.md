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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385940"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="74bd2-103">Propriedade canônica PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="74bd2-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="74bd2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74bd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74bd2-105">Contém a hora em que o contêiner de pasta de pesquisa estarão obsoleto e devem ser atualizados ou recriados.</span><span class="sxs-lookup"><span data-stu-id="74bd2-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74bd2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="74bd2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74bd2-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="74bd2-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="74bd2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74bd2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74bd2-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="74bd2-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="74bd2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="74bd2-110">Data type:</span></span>  <br/> |<span data-ttu-id="74bd2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74bd2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74bd2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74bd2-112">Area:</span></span>  <br/> |<span data-ttu-id="74bd2-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="74bd2-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74bd2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74bd2-114">Remarks</span></span>

<span data-ttu-id="74bd2-115">Esta propriedade deve ser formatada como o número de minutos desde a meia-noite Tempo Universal Coordenado (UTC) em 1 de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="74bd2-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74bd2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74bd2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74bd2-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="74bd2-117">Protocol specifications</span></span>

<span data-ttu-id="74bd2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74bd2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74bd2-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="74bd2-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74bd2-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74bd2-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74bd2-121">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="74bd2-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74bd2-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="74bd2-122">Header files</span></span>

<span data-ttu-id="74bd2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74bd2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="74bd2-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="74bd2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="74bd2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74bd2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="74bd2-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="74bd2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74bd2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="74bd2-127">See also</span></span>



[<span data-ttu-id="74bd2-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74bd2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74bd2-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="74bd2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74bd2-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="74bd2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74bd2-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="74bd2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

