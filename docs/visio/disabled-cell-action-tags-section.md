---
title: Célula Disabled (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indica se a marca de ação é exibida na janela de desenho.
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332561"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="18aa9-103">Célula Disabled (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="18aa9-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="18aa9-104">Indica se a marca de ação é exibida na janela de desenho.</span><span class="sxs-lookup"><span data-stu-id="18aa9-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="18aa9-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="18aa9-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="18aa9-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="18aa9-106">**Value**</span></span>|<span data-ttu-id="18aa9-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18aa9-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="18aa9-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="18aa9-108">TRUE</span></span>  <br/> | <span data-ttu-id="18aa9-109">A marca de ação está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="18aa9-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="18aa9-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="18aa9-110">FALSE</span></span>  <br/> | <span data-ttu-id="18aa9-111">A marca de ação está habilitada (padrão).</span><span class="sxs-lookup"><span data-stu-id="18aa9-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18aa9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="18aa9-112">Remarks</span></span>

<span data-ttu-id="18aa9-113">Quando uma marca de ação está desabilitada, ela não é exibida até ser reabilitada.</span><span class="sxs-lookup"><span data-stu-id="18aa9-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="18aa9-114">Para fazer referência à célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="18aa9-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18aa9-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="18aa9-115">Cell name:</span></span>  <br/> | <span data-ttu-id="18aa9-116">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="18aa9-116">SmartTags.</span></span>  <span data-ttu-id="18aa9-117">*nome* . Desativado onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="18aa9-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="18aa9-118">*name*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="18aa9-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="18aa9-119">Para fazer referência à célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="18aa9-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18aa9-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="18aa9-120">Section index:</span></span>  <br/> |<span data-ttu-id="18aa9-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="18aa9-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="18aa9-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="18aa9-122">Row index:</span></span>  <br/> |<span data-ttu-id="18aa9-123">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="18aa9-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="18aa9-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="18aa9-124">Cell index:</span></span>  <br/> |<span data-ttu-id="18aa9-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="18aa9-125">**visSmartTagDisabled**</span></span> <br/> |
   

