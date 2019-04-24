---
title: Célula PagesY (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Determina o número de páginas impressas nas quais será ajustada verticalmente a página de desenho.
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339974"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="41e7e-103">Célula PagesY (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="41e7e-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="41e7e-104">Determina o número de páginas impressas nas quais será ajustada verticalmente a página de desenho.</span><span class="sxs-lookup"><span data-stu-id="41e7e-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41e7e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="41e7e-105">Remarks</span></span>

<span data-ttu-id="41e7e-106">Esse valor é usado somente quando a célula OnPage está definida como VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="41e7e-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="41e7e-107">Para fazer referência à célula PagesY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="41e7e-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41e7e-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="41e7e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="41e7e-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="41e7e-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="41e7e-110">Para fazer referência à célula PagesY pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="41e7e-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41e7e-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="41e7e-111">Section index:</span></span>  <br/> |<span data-ttu-id="41e7e-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41e7e-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="41e7e-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="41e7e-113">Row index:</span></span>  <br/> |<span data-ttu-id="41e7e-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="41e7e-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="41e7e-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="41e7e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="41e7e-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="41e7e-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

