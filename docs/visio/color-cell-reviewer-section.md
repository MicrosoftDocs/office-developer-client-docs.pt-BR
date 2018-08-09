---
title: Célula Color (Seção Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Um valor RGB que representa a cor atribuída à marcação do revisor de um documento.
ms.openlocfilehash: a8771bb35cfc1b57990f24e1a0a3d677f9cffc0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771522"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="b372a-103">Célula Color (Seção Reviewer)</span><span class="sxs-lookup"><span data-stu-id="b372a-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="b372a-104">Um valor RGB que representa a cor atribuída à marcação do revisor de um documento.</span><span class="sxs-lookup"><span data-stu-id="b372a-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b372a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b372a-105">Remarks</span></span>

<span data-ttu-id="b372a-p101">As cores são atribuídas aos revisores nesta sequência: vermelho, azul, verde, violeta, laranja, turquesa, cinza. Elas são utilizadas em sequência novamente para os revisores restantes.</span><span class="sxs-lookup"><span data-stu-id="b372a-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="b372a-108">Os comentários inseridos na página de desenho original são sempre em amarelo, independente da cor atribuída a um revisor na célula Color.</span><span class="sxs-lookup"><span data-stu-id="b372a-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="b372a-109">Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b372a-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b372a-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b372a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b372a-111">Reviewer. Color [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b372a-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b372a-112">Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b372a-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b372a-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b372a-113">Section index:</span></span>  <br/> |<span data-ttu-id="b372a-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="b372a-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="b372a-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b372a-115">Row index:</span></span>  <br/> |<span data-ttu-id="b372a-116">**visRowReviewer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b372a-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b372a-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b372a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b372a-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="b372a-118">**visReviewerColor**</span></span> <br/> |
   

