---
title: Propriedade canônica PidTagControlStructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769121"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="b6699-103">Propriedade canônica PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="b6699-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="b6699-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6699-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6699-105">Contém um ponteiro para uma estrutura para um controle usado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b6699-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6699-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b6699-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6699-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="b6699-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="b6699-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b6699-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6699-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="b6699-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="b6699-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b6699-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6699-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b6699-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b6699-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b6699-112">Area:</span></span>  <br/> |<span data-ttu-id="b6699-113">Tabela de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="b6699-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6699-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6699-114">Remarks</span></span>

<span data-ttu-id="b6699-115">Essa propriedade representa um ponteiro long que é convertido em uma das estruturas de controle.</span><span class="sxs-lookup"><span data-stu-id="b6699-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="b6699-116">As estruturas de controle incluem:</span><span class="sxs-lookup"><span data-stu-id="b6699-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="b6699-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="b6699-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="b6699-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="b6699-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="b6699-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="b6699-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="b6699-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="b6699-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="b6699-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="b6699-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="b6699-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="b6699-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="b6699-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="b6699-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="b6699-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="b6699-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="b6699-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="b6699-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="b6699-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="b6699-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="b6699-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="b6699-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="b6699-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="b6699-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b6699-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6699-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b6699-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b6699-130">Header files</span></span>

<span data-ttu-id="b6699-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6699-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6699-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b6699-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6699-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6699-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b6699-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b6699-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6699-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6699-135">See also</span></span>



[<span data-ttu-id="b6699-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b6699-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6699-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b6699-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6699-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b6699-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6699-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b6699-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

