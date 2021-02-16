---
title: Propriedade canônica PidTagSearchFolderTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b7a88387-72ff-49e5-b73a-8bafab635658
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a4ad72c147abebfe9863d19690bc9f27f00544a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282317"
---
# <a name="pidtagsearchfoldertag-canonical-property"></a><span data-ttu-id="c034a-103">Propriedade canônica PidTagSearchFolderTag</span><span class="sxs-lookup"><span data-stu-id="c034a-103">PidTagSearchFolderTag Canonical Property</span></span>

  
  
<span data-ttu-id="c034a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c034a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c034a-105">Contém o valor usado para sincronizar essa mensagem de definição com o contêiner de pasta de pesquisa correspondente.</span><span class="sxs-lookup"><span data-stu-id="c034a-105">Contains the value used to synchronize this definition message with the matching search folder container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c034a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c034a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c034a-107">PR_WB_SF_TAG</span><span class="sxs-lookup"><span data-stu-id="c034a-107">PR_WB_SF_TAG</span></span>  <br/> |
|<span data-ttu-id="c034a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c034a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c034a-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="c034a-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="c034a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c034a-110">Data type:</span></span>  <br/> |<span data-ttu-id="c034a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c034a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c034a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c034a-112">Area:</span></span>  <br/> |<span data-ttu-id="c034a-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="c034a-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c034a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c034a-114">Remarks</span></span>

<span data-ttu-id="c034a-115">Essa propriedade é alterada quando a mensagem de definição é alterada.</span><span class="sxs-lookup"><span data-stu-id="c034a-115">This property is changed when the definition message is changed.</span></span> <span data-ttu-id="c034a-116">Ela deve alterar cada iteração, mas pode não ser exclusiva.</span><span class="sxs-lookup"><span data-stu-id="c034a-116">It must change each iteration, but it may not be unique.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c034a-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c034a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c034a-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c034a-118">Protocol specifications</span></span>

<span data-ttu-id="c034a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c034a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c034a-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c034a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c034a-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c034a-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c034a-122">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c034a-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c034a-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="c034a-123">Header files</span></span>

<span data-ttu-id="c034a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c034a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c034a-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c034a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c034a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c034a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c034a-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c034a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c034a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c034a-128">See also</span></span>



[<span data-ttu-id="c034a-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c034a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c034a-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c034a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c034a-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c034a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c034a-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c034a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

