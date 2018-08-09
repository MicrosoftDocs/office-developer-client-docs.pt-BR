---
title: Célula PageBottomMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Especifica a margem inferior da página.
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772444"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="0512e-103">Célula PageBottomMargin (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="0512e-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="0512e-104">Especifica a margem inferior da página.</span><span class="sxs-lookup"><span data-stu-id="0512e-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0512e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0512e-105">Remarks</span></span>

<span data-ttu-id="0512e-p101">Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,5 pol., essa margem será 0,5 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página.</span><span class="sxs-lookup"><span data-stu-id="0512e-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="0512e-109">Para fazer referência à célula PageBottomMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0512e-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0512e-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0512e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="0512e-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="0512e-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="0512e-112">Para fazer referência à célula PageBottomMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0512e-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0512e-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0512e-113">Section index:</span></span>  <br/> |<span data-ttu-id="0512e-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0512e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0512e-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0512e-115">Row index:</span></span>  <br/> |<span data-ttu-id="0512e-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="0512e-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="0512e-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0512e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="0512e-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="0512e-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

