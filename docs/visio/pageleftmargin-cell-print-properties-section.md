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
ms.openlocfilehash: 5fd2c8cd5b18a4baedd355627005b7c5c2df3252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772445"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="dba6e-103">Célula PageLeftMargin (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="dba6e-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="dba6e-104">Especifica a margem esquerda da página.</span><span class="sxs-lookup"><span data-stu-id="dba6e-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dba6e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="dba6e-105">Remarks</span></span>

<span data-ttu-id="dba6e-p101">Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,25 pol., essa margem será 0,25 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página.</span><span class="sxs-lookup"><span data-stu-id="dba6e-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="dba6e-109">Para fazer referência à célula PageLeftMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="dba6e-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dba6e-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="dba6e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="dba6e-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="dba6e-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="dba6e-112">Para fazer referência à célula PageLeftMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="dba6e-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dba6e-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="dba6e-113">Section index:</span></span>  <br/> |<span data-ttu-id="dba6e-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dba6e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dba6e-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="dba6e-115">Row index:</span></span>  <br/> |<span data-ttu-id="dba6e-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="dba6e-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="dba6e-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="dba6e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="dba6e-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="dba6e-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

