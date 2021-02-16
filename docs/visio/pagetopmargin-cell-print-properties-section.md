---
title: Célula PageTopMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Especifica a margem superior da página impressa.
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416577"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="0cd0d-103">Célula PageTopMargin (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="0cd0d-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="0cd0d-104">Especifica a margem superior da página impressa.</span><span class="sxs-lookup"><span data-stu-id="0cd0d-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cd0d-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cd0d-105">Remarks</span></span>

<span data-ttu-id="0cd0d-p101">Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,25 pol., essa margem será 0,25 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página.</span><span class="sxs-lookup"><span data-stu-id="0cd0d-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="0cd0d-109">Para fazer referência à célula PageTopMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0cd0d-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cd0d-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0cd0d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="0cd0d-111">PageTopMargin</span><span class="sxs-lookup"><span data-stu-id="0cd0d-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="0cd0d-112">Para fazer referência à célula PageTopMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0cd0d-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cd0d-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0cd0d-113">Section index:</span></span>  <br/> |<span data-ttu-id="0cd0d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0cd0d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0cd0d-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="0cd0d-115">Row index:</span></span>  <br/> |<span data-ttu-id="0cd0d-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="0cd0d-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="0cd0d-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0cd0d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="0cd0d-118">**visPrintPropertiesTopMargin**</span><span class="sxs-lookup"><span data-stu-id="0cd0d-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

