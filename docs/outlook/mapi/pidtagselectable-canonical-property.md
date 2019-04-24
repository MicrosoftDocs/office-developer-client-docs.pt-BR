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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359014"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="33af9-103">Propriedade canônica PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="33af9-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="33af9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33af9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33af9-105">Contém TRUE se a entrada na tabela one-off pode ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="33af9-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33af9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="33af9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33af9-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="33af9-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="33af9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="33af9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33af9-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="33af9-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="33af9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="33af9-110">Data type:</span></span>  <br/> |<span data-ttu-id="33af9-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="33af9-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="33af9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="33af9-112">Area:</span></span>  <br/> |<span data-ttu-id="33af9-113">Contêiner de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="33af9-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33af9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="33af9-114">Remarks</span></span>

<span data-ttu-id="33af9-115">Essa propriedade é usada principalmente para formatação visual de uma tabela única.</span><span class="sxs-lookup"><span data-stu-id="33af9-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="33af9-116">Os modelos podem ser agrupados criando uma entrada que indica o título do grupo.</span><span class="sxs-lookup"><span data-stu-id="33af9-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="33af9-117">A definição dessa propriedade como FALSE para o título garante que o usuário possa selecionar apenas os modelos reais no grupo e não esta entrada de título.</span><span class="sxs-lookup"><span data-stu-id="33af9-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="33af9-118">Essa propriedade só se aplica a uma tabela única, e não a uma tabela de hierarquia de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="33af9-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="33af9-119">O MAPI permite que um provedor de catálogo de endereços agrupe itens visualmente por dois meios.</span><span class="sxs-lookup"><span data-stu-id="33af9-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="33af9-120">Primeiro, determinadas linhas podem funcionar como títulos ao serem não-selecionadas.</span><span class="sxs-lookup"><span data-stu-id="33af9-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="33af9-121">Segundo, os itens selecionáveis podem ser recuados em relação aos seus títulos usando a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33af9-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="33af9-122">Essa propriedade é usada nesse agrupamento para indicar se este item pode ou não ser selecionado de uma lista para criar um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="33af9-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="33af9-123">Por exemplo, se um cliente tiver vários modelos para a criação de endereços de fax, ele poderá exibi-los da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="33af9-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="33af9-124">Modelos de FAX (profundidade 0, não selecionável)</span><span class="sxs-lookup"><span data-stu-id="33af9-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="33af9-125">Local (profundidade 1, selecionável)</span><span class="sxs-lookup"><span data-stu-id="33af9-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="33af9-126">Longa distância (profundidade 1, selecionável)</span><span class="sxs-lookup"><span data-stu-id="33af9-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33af9-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="33af9-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33af9-128">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="33af9-128">Protocol specifications</span></span>

<span data-ttu-id="33af9-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33af9-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33af9-130">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="33af9-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33af9-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33af9-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33af9-132">Especifica as propriedades e as operações que são permitidas para os modelos de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="33af9-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33af9-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="33af9-133">Header files</span></span>

<span data-ttu-id="33af9-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="33af9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="33af9-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="33af9-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="33af9-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="33af9-136">Mapitags.h</span></span>
  
> <span data-ttu-id="33af9-137">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="33af9-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33af9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="33af9-138">See also</span></span>



[<span data-ttu-id="33af9-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="33af9-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="33af9-140">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="33af9-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="33af9-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="33af9-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33af9-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="33af9-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33af9-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="33af9-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33af9-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="33af9-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

