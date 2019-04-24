---
title: Célula Width (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Contém a largura da forma selecionada em unidades de desenho. A fórmula padrão para determinar a largura de uma forma 1D é:'
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351216"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="d2d04-104">Célula Width (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="d2d04-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="d2d04-105">Contém a largura da forma selecionada em unidades de desenho.</span><span class="sxs-lookup"><span data-stu-id="d2d04-105">Contains the width of the selected shape in drawing units.</span></span> <span data-ttu-id="d2d04-106">A fórmula padrão para determinar a largura de uma forma 1D é:</span><span class="sxs-lookup"><span data-stu-id="d2d04-106">The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="d2d04-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="d2d04-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2d04-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2d04-108">Remarks</span></span>

<span data-ttu-id="d2d04-109">Para fazer referência à célula Width pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d2d04-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2d04-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d2d04-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d2d04-111">Largura</span><span class="sxs-lookup"><span data-stu-id="d2d04-111">Width</span></span>  <br/> |
   
<span data-ttu-id="d2d04-112">Para fazer referência à célula Width pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d2d04-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2d04-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d2d04-113">Section index:</span></span>  <br/> |<span data-ttu-id="d2d04-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2d04-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2d04-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d2d04-115">Row index:</span></span>  <br/> |<span data-ttu-id="d2d04-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="d2d04-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="d2d04-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d2d04-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d2d04-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="d2d04-118">**visXFormWidth**</span></span> <br/> |
   

