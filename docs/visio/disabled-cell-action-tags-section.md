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
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771718"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="5a56f-103">Célula Disabled (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="5a56f-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="5a56f-104">Indica se a marca de ação é exibida na janela de desenho.</span><span class="sxs-lookup"><span data-stu-id="5a56f-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5a56f-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="5a56f-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="5a56f-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5a56f-106">**Value**</span></span>|<span data-ttu-id="5a56f-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a56f-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5a56f-108">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="5a56f-108">TRUE</span></span>  <br/> | <span data-ttu-id="5a56f-109">A marca de ação está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="5a56f-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="5a56f-110">FALSO</span><span class="sxs-lookup"><span data-stu-id="5a56f-110">FALSE</span></span>  <br/> | <span data-ttu-id="5a56f-111">A marca de ação está habilitada (padrão).</span><span class="sxs-lookup"><span data-stu-id="5a56f-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a56f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a56f-112">Remarks</span></span>

<span data-ttu-id="5a56f-113">Quando uma marca de ação está desabilitada, ela não é exibida até ser reabilitada.</span><span class="sxs-lookup"><span data-stu-id="5a56f-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="5a56f-114">Para fazer referência à célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="5a56f-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a56f-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5a56f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5a56f-116">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="5a56f-116">SmartTags.</span></span>  <span data-ttu-id="5a56f-117">*nome* . Desabilitado onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="5a56f-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="5a56f-118">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="5a56f-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="5a56f-119">Para obter uma referência para a célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5a56f-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a56f-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5a56f-120">Section index:</span></span>  <br/> |<span data-ttu-id="5a56f-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="5a56f-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="5a56f-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5a56f-122">Row index:</span></span>  <br/> |<span data-ttu-id="5a56f-123">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5a56f-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5a56f-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5a56f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5a56f-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="5a56f-125">**visSmartTagDisabled**</span></span> <br/> |
   

