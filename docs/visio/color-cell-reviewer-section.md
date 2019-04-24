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
description: Um valor RGB que representa a cor atribuída à marcação de um revisor de documento.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341815"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="d50a1-103">Célula Color (Seção Reviewer)</span><span class="sxs-lookup"><span data-stu-id="d50a1-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="d50a1-104">Um valor RGB que representa a cor atribuída à marcação de um revisor de documento.</span><span class="sxs-lookup"><span data-stu-id="d50a1-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d50a1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d50a1-105">Remarks</span></span>

<span data-ttu-id="d50a1-p101">As cores são atribuídas aos revisores nesta sequência: vermelho, azul, verde, violeta, laranja, turquesa, cinza. Elas são utilizadas em sequência novamente para os revisores restantes.</span><span class="sxs-lookup"><span data-stu-id="d50a1-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="d50a1-108">Os comentários inseridos na página de desenho original são sempre em amarelo, independente da cor atribuída a um revisor na célula Color.</span><span class="sxs-lookup"><span data-stu-id="d50a1-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="d50a1-109">Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d50a1-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d50a1-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d50a1-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d50a1-111">Reviewer. Color [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d50a1-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d50a1-112">Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d50a1-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d50a1-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d50a1-113">Section index:</span></span>  <br/> |<span data-ttu-id="d50a1-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="d50a1-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="d50a1-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d50a1-115">Row index:</span></span>  <br/> |<span data-ttu-id="d50a1-116">**visRowReviewer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d50a1-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d50a1-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d50a1-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d50a1-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="d50a1-118">**visReviewerColor**</span></span> <br/> |
   

