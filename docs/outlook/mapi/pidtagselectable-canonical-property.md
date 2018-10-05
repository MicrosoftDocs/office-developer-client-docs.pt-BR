---
title: Propriedade canônica PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383454"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="9bbea-103">Propriedade canônica PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="9bbea-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="9bbea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bbea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bbea-105">Conterá TRUE se a entrada na tabela único pode ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="9bbea-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bbea-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9bbea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bbea-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="9bbea-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="9bbea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9bbea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bbea-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="9bbea-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="9bbea-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9bbea-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bbea-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9bbea-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9bbea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9bbea-112">Area:</span></span>  <br/> |<span data-ttu-id="9bbea-113">Contêiner de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="9bbea-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bbea-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bbea-114">Remarks</span></span>

<span data-ttu-id="9bbea-115">Essa propriedade é usada principalmente para formatação visual de uma tabela único.</span><span class="sxs-lookup"><span data-stu-id="9bbea-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="9bbea-116">Modelos podem ser agrupados, criando uma entrada que indica o título para o grupo.</span><span class="sxs-lookup"><span data-stu-id="9bbea-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="9bbea-117">A definição dessa propriedade como FALSE para o título garante que o usuário pode selecionar somente os modelos de reais do grupo e não essa entrada de título.</span><span class="sxs-lookup"><span data-stu-id="9bbea-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="9bbea-118">Essa propriedade só se aplica a uma tabela único, não em uma tabela de hierarquia de catálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="9bbea-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="9bbea-119">MAPI permite visualmente um provedor de catálogo de endereços para agrupar itens por meio de duas.</span><span class="sxs-lookup"><span data-stu-id="9bbea-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="9bbea-120">Em primeiro lugar, determinadas linhas podem funcionar como títulos por sendo não-selecionável.</span><span class="sxs-lookup"><span data-stu-id="9bbea-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="9bbea-121">Em segundo lugar, os itens selecionável podem ser recuados em relação ao seus títulos usando a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9bbea-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="9bbea-122">Essa propriedade é usada em tal agrupamento para indicar se ou não esse item pode ser selecionado em uma lista para criar um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="9bbea-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="9bbea-123">Por exemplo, se um cliente tiver vários modelos para construir endereços de fax, ele poderá exibi-las da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9bbea-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="9bbea-124">Modelos de FAX (profundidade 0, não selecionável)</span><span class="sxs-lookup"><span data-stu-id="9bbea-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="9bbea-125">Local (profundidade 1, selecionável)</span><span class="sxs-lookup"><span data-stu-id="9bbea-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="9bbea-126">Longa distância (profundidade 1, selecionável)</span><span class="sxs-lookup"><span data-stu-id="9bbea-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9bbea-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bbea-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bbea-128">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9bbea-128">Protocol specifications</span></span>

<span data-ttu-id="9bbea-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bbea-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bbea-130">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9bbea-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bbea-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bbea-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bbea-132">Especifica as propriedades e operações que são permitidas para modelos de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="9bbea-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bbea-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9bbea-133">Header files</span></span>

<span data-ttu-id="9bbea-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bbea-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bbea-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9bbea-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bbea-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9bbea-136">Mapitags.h</span></span>
  
> <span data-ttu-id="9bbea-137">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="9bbea-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bbea-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bbea-138">See also</span></span>



[<span data-ttu-id="9bbea-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="9bbea-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="9bbea-140">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="9bbea-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="9bbea-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9bbea-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bbea-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9bbea-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bbea-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9bbea-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bbea-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9bbea-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

