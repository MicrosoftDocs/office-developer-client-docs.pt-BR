---
title: Célula PageRightMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Especifica a margem direita da página impressa.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440007"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="ffb32-103">Célula PageRightMargin (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="ffb32-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="ffb32-104">Especifica a margem direita da página impressa.</span><span class="sxs-lookup"><span data-stu-id="ffb32-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffb32-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffb32-105">Remarks</span></span>

<span data-ttu-id="ffb32-p101">Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,25 pol., essa margem será 0,25 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página.</span><span class="sxs-lookup"><span data-stu-id="ffb32-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="ffb32-109">Para fazer referência à célula PageRightMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ffb32-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffb32-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ffb32-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ffb32-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="ffb32-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="ffb32-112">Para fazer referência à célula PageRightMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ffb32-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffb32-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ffb32-113">Section index:</span></span>  <br/> |<span data-ttu-id="ffb32-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ffb32-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ffb32-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ffb32-115">Row index:</span></span>  <br/> |<span data-ttu-id="ffb32-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="ffb32-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="ffb32-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ffb32-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ffb32-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="ffb32-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

