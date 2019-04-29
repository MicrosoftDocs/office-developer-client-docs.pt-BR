---
title: Célula PageLeftMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Especifica a margem esquerda da página.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435667"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="51ca9-103">Célula PageLeftMargin (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="51ca9-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="51ca9-104">Especifica a margem esquerda da página.</span><span class="sxs-lookup"><span data-stu-id="51ca9-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51ca9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="51ca9-105">Remarks</span></span>

<span data-ttu-id="51ca9-p101">Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,25 pol., essa margem será 0,25 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página.</span><span class="sxs-lookup"><span data-stu-id="51ca9-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="51ca9-109">Para fazer referência à célula PageLeftMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="51ca9-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51ca9-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="51ca9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="51ca9-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="51ca9-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="51ca9-112">Para fazer referência à célula PageLeftMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="51ca9-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51ca9-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="51ca9-113">Section index:</span></span>  <br/> |<span data-ttu-id="51ca9-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51ca9-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51ca9-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="51ca9-115">Row index:</span></span>  <br/> |<span data-ttu-id="51ca9-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="51ca9-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="51ca9-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="51ca9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="51ca9-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="51ca9-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

