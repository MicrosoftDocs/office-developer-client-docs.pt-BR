---
title: Célula PagesX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Determina o número de páginas impressas nas quais será ajustada horizontalmente a página de desenho.
ms.openlocfilehash: 4f1cf3286e7b54dc90925bf2f1ab9fe8532022e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772465"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="7ffb2-103">Célula PagesX (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="7ffb2-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="7ffb2-104">Determina o número de páginas impressas nas quais será ajustada horizontalmente a página de desenho.</span><span class="sxs-lookup"><span data-stu-id="7ffb2-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7ffb2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ffb2-105">Remarks</span></span>

<span data-ttu-id="7ffb2-106">Esse valor é usado somente quando a célula OnPage está definida como VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="7ffb2-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="7ffb2-107">Para fazer referência à célula PagesX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7ffb2-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ffb2-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7ffb2-108">Cell name:</span></span>  <br/> | <span data-ttu-id="7ffb2-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="7ffb2-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="7ffb2-110">Para fazer referência à célula PagesX pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7ffb2-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ffb2-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7ffb2-111">Section index:</span></span>  <br/> |<span data-ttu-id="7ffb2-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7ffb2-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7ffb2-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7ffb2-113">Row index:</span></span>  <br/> |<span data-ttu-id="7ffb2-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="7ffb2-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="7ffb2-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7ffb2-115">Cell index:</span></span>  <br/> |<span data-ttu-id="7ffb2-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="7ffb2-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

