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
ms.openlocfilehash: 3b517888d562ee5b178dbd011fa1ce6ab218c6b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594352"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="4d45f-103">Propriedade canônica PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="4d45f-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="4d45f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d45f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d45f-105">Contém um ponteiro para uma estrutura para um controle usado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4d45f-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d45f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4d45f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d45f-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="4d45f-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="4d45f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4d45f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d45f-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="4d45f-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="4d45f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4d45f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d45f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4d45f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4d45f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4d45f-112">Area:</span></span>  <br/> |<span data-ttu-id="4d45f-113">Tabela de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="4d45f-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d45f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d45f-114">Remarks</span></span>

<span data-ttu-id="4d45f-115">Essa propriedade representa um ponteiro long que é convertido em uma das estruturas de controle.</span><span class="sxs-lookup"><span data-stu-id="4d45f-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="4d45f-116">As estruturas de controle incluem:</span><span class="sxs-lookup"><span data-stu-id="4d45f-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="4d45f-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="4d45f-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="4d45f-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="4d45f-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="4d45f-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="4d45f-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="4d45f-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="4d45f-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="4d45f-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="4d45f-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="4d45f-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="4d45f-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="4d45f-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="4d45f-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="4d45f-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="4d45f-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="4d45f-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="4d45f-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="4d45f-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="4d45f-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="4d45f-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="4d45f-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="4d45f-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="4d45f-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4d45f-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d45f-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4d45f-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4d45f-130">Header files</span></span>

<span data-ttu-id="4d45f-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d45f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d45f-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4d45f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d45f-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d45f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="4d45f-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4d45f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d45f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d45f-135">See also</span></span>



[<span data-ttu-id="4d45f-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d45f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d45f-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4d45f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d45f-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4d45f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d45f-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4d45f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

