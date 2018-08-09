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
ms.openlocfilehash: e98416ba7796c66d719adcc27ba8029b7908bb79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770004"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="79632-103">Propriedade canônica PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="79632-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="79632-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79632-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79632-105">Contém os sinalizadores de pasta estendida que se aplicam para o contêiner de pasta de pesquisa para a pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="79632-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79632-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="79632-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79632-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="79632-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="79632-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="79632-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79632-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="79632-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="79632-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="79632-110">Data type:</span></span>  <br/> |<span data-ttu-id="79632-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="79632-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="79632-112">Área:</span><span class="sxs-lookup"><span data-stu-id="79632-112">Area:</span></span>  <br/> |<span data-ttu-id="79632-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="79632-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79632-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="79632-114">Remarks</span></span>

<span data-ttu-id="79632-115">Essa propriedade especificamente deve conter os sinalizadores a propriedade **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) e a propriedade sub-recurso **ExtendedFlags** , no campo b para a pasta.</span><span class="sxs-lookup"><span data-stu-id="79632-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="79632-116">Para obter informações sobre os sinalizadores de pasta, consulte o [[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="79632-116">For information about folder flags see the [[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="79632-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="79632-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79632-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="79632-118">Protocol specifications</span></span>

<span data-ttu-id="79632-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79632-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79632-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="79632-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79632-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79632-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79632-122">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="79632-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="79632-123">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79632-123">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79632-124">Especifica o local e as propriedades de dados de configuração de cliente e servidor, como listas de categoria compartilhada e o horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79632-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79632-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="79632-125">Header files</span></span>

<span data-ttu-id="79632-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79632-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="79632-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="79632-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="79632-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="79632-128">Mapitags.h</span></span>
  
> <span data-ttu-id="79632-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="79632-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79632-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="79632-130">See also</span></span>



[<span data-ttu-id="79632-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="79632-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79632-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="79632-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79632-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="79632-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79632-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="79632-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

