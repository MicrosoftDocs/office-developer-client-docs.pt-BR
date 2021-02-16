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
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="67355-103">Propriedade canônica PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="67355-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="67355-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67355-105">Contém sinalizadores de pasta estendida que se aplicam ao contêiner da pasta de pesquisa para a pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="67355-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67355-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="67355-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67355-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="67355-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="67355-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="67355-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67355-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="67355-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="67355-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="67355-110">Data type:</span></span>  <br/> |<span data-ttu-id="67355-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="67355-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="67355-112">Área:</span><span class="sxs-lookup"><span data-stu-id="67355-112">Area:</span></span>  <br/> |<span data-ttu-id="67355-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="67355-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67355-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67355-114">Remarks</span></span>

<span data-ttu-id="67355-115">Essa propriedade deve conter especificamente os sinalizadores na propriedade **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) e a sub-propriedade **ExtendedFlags,** no campo b da pasta.</span><span class="sxs-lookup"><span data-stu-id="67355-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="67355-116">Para obter informações sobre sinalizadores de pasta, consulte [o [MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="67355-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67355-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="67355-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67355-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="67355-118">Protocol specifications</span></span>

<span data-ttu-id="67355-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67355-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67355-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="67355-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67355-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67355-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67355-122">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="67355-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="67355-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67355-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67355-124">Especifica o local e as propriedades dos dados de configuração do cliente e do servidor, como listas de categorias compartilhadas e horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="67355-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67355-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="67355-125">Header files</span></span>

<span data-ttu-id="67355-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67355-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="67355-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="67355-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="67355-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67355-128">Mapitags.h</span></span>
  
> <span data-ttu-id="67355-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="67355-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67355-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="67355-130">See also</span></span>



[<span data-ttu-id="67355-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="67355-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67355-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="67355-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67355-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="67355-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67355-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="67355-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

