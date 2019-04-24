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
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334409"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="94289-103">Célula PageBottomMargin (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="94289-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="94289-104">Especifica a margem inferior da página.</span><span class="sxs-lookup"><span data-stu-id="94289-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94289-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="94289-105">Remarks</span></span>

<span data-ttu-id="94289-p101">Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,5 pol., essa margem será 0,5 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página.</span><span class="sxs-lookup"><span data-stu-id="94289-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="94289-109">Para fazer referência à célula PageBottomMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="94289-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94289-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="94289-110">Cell name:</span></span>  <br/> | <span data-ttu-id="94289-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="94289-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="94289-112">Para fazer referência à célula PageBottomMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="94289-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94289-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="94289-113">Section index:</span></span>  <br/> |<span data-ttu-id="94289-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94289-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="94289-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="94289-115">Row index:</span></span>  <br/> |<span data-ttu-id="94289-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="94289-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="94289-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="94289-117">Cell index:</span></span>  <br/> |<span data-ttu-id="94289-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="94289-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

