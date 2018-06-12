---
title: Propriedade canônico de PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769870"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="99feb-103">Propriedade canônico de PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="99feb-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="99feb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99feb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99feb-105">Contém um valor que indica o tipo de uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="99feb-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99feb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="99feb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99feb-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="99feb-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="99feb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="99feb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="99feb-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="99feb-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="99feb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="99feb-110">Data type:</span></span>  <br/> |<span data-ttu-id="99feb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="99feb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="99feb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="99feb-112">Area:</span></span>  <br/> |<span data-ttu-id="99feb-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="99feb-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99feb-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="99feb-114">Remarks</span></span>

<span data-ttu-id="99feb-115">Essa propriedade é exibida somente nas tabelas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="99feb-115">This property appears only on contents tables.</span></span> <span data-ttu-id="99feb-116">Só existe uma categoria quando ele tem itens.</span><span class="sxs-lookup"><span data-stu-id="99feb-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="99feb-117">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="99feb-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="99feb-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="99feb-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="99feb-119">Representa os dados reais, em vez de uma linha de categoria.</span><span class="sxs-lookup"><span data-stu-id="99feb-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="99feb-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="99feb-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="99feb-121">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="99feb-121">Not currently used.</span></span>
    
<span data-ttu-id="99feb-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="99feb-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="99feb-123">A categoria é expandida; a interface do usuário geralmente exibe isso com o sinal de menos (-) ao lado dela.</span><span class="sxs-lookup"><span data-stu-id="99feb-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="99feb-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="99feb-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="99feb-125">A categoria estiver recolhida; a interface do usuário geralmente exibe isso com o sinal de adição (+) ao lado dela.</span><span class="sxs-lookup"><span data-stu-id="99feb-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="99feb-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="99feb-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99feb-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="99feb-127">Protocol specifications</span></span>

<span data-ttu-id="99feb-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99feb-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99feb-129">Inclui as operações permitidas para os objetos de tabela principal.</span><span class="sxs-lookup"><span data-stu-id="99feb-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99feb-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99feb-130">Header files</span></span>

<span data-ttu-id="99feb-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99feb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="99feb-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="99feb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="99feb-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="99feb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="99feb-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="99feb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99feb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="99feb-135">See also</span></span>



[<span data-ttu-id="99feb-136">Propriedade canônico de PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="99feb-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="99feb-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="99feb-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99feb-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="99feb-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99feb-139">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="99feb-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99feb-140">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="99feb-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

