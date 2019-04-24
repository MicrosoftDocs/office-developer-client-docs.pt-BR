---
title: Propriedade canônica PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336425"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="f6888-103">Propriedade canônica PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="f6888-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f6888-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6888-105">Contém sinalizadores de pasta estendida que se aplicam ao contêiner da pasta de pesquisa da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f6888-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6888-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f6888-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6888-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f6888-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f6888-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f6888-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6888-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="f6888-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="f6888-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f6888-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6888-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f6888-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f6888-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f6888-112">Area:</span></span>  <br/> |<span data-ttu-id="f6888-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="f6888-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6888-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6888-114">Remarks</span></span>

<span data-ttu-id="f6888-115">Essa propriedade deve conter especificamente os sinalizadores na propriedade **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) e a subpropriedade **ExtendedFlags** , no campo b da pasta.</span><span class="sxs-lookup"><span data-stu-id="f6888-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="f6888-116">Para obter informações sobre sinalizadores de pasta, consulte [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6888-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f6888-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6888-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6888-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="f6888-118">Protocol specifications</span></span>

<span data-ttu-id="f6888-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6888-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6888-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f6888-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f6888-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6888-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6888-122">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f6888-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="f6888-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6888-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6888-124">Especifica o local e as propriedades dos dados de configuração de cliente e de servidor, como listas de categorias compartilhadas e horários de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f6888-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6888-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6888-125">Header files</span></span>

<span data-ttu-id="f6888-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f6888-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6888-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f6888-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6888-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f6888-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f6888-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f6888-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6888-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6888-130">See also</span></span>



[<span data-ttu-id="f6888-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f6888-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6888-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f6888-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6888-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f6888-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6888-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f6888-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

