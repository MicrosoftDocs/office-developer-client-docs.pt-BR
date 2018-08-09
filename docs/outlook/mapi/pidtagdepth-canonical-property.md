---
title: Propriedade canônica PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769169"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="5a931-103">Propriedade canônica PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="5a931-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="5a931-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a931-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a931-105">Contém um número inteiro que representa o nível relativo de recuo ou profundidade, de um objeto em uma tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="5a931-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a931-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5a931-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a931-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="5a931-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="5a931-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a931-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a931-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="5a931-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="5a931-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5a931-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a931-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5a931-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5a931-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5a931-112">Area:</span></span>  <br/> |<span data-ttu-id="5a931-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="5a931-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a931-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a931-114">Remarks</span></span>

<span data-ttu-id="5a931-115">Essa propriedade também pode especificar o nível de categorização de uma linha em uma tabela de conteúdo ou a profundidade da hierarquia em uma tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="5a931-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="5a931-116">A intensidade é baseado em zero, onde zero representa a categoria mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="5a931-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="5a931-117">Em todos os casos, o valor da propriedade representa um valor relativo em vez de um valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="5a931-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="5a931-118">Na tabela de hierarquia, por exemplo, o valor de profundidade é em relação ao contêiner do qual a tabela de hierarquia foi recuperada.</span><span class="sxs-lookup"><span data-stu-id="5a931-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="5a931-119">A intensidade do contêiner raiz não representa uma profundidade absoluta.</span><span class="sxs-lookup"><span data-stu-id="5a931-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a931-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a931-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a931-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5a931-121">Protocol specifications</span></span>

<span data-ttu-id="5a931-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a931-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a931-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5a931-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a931-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a931-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a931-125">Inclui as operações permitidas para os objetos de tabela principal.</span><span class="sxs-lookup"><span data-stu-id="5a931-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="5a931-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a931-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a931-127">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="5a931-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a931-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5a931-128">Header files</span></span>

<span data-ttu-id="5a931-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a931-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a931-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5a931-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a931-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a931-131">Mapitags.h</span></span>
  
> <span data-ttu-id="5a931-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5a931-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a931-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a931-133">See also</span></span>



[<span data-ttu-id="5a931-134">Propriedade canônica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="5a931-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="5a931-135">Propriedade canônica PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="5a931-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="5a931-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a931-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a931-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5a931-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a931-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5a931-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a931-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5a931-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
