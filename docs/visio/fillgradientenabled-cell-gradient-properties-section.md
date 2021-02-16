---
title: Célula FillGradientEnabled (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Determina se um gradiente de preenchimento está habilitado para essa forma.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431208"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="cd5e3-103">Célula FillGradientEnabled (Seção Gradient Properties)</span><span class="sxs-lookup"><span data-stu-id="cd5e3-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="cd5e3-104">Determina se um gradiente de preenchimento está habilitado para essa forma.</span><span class="sxs-lookup"><span data-stu-id="cd5e3-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="cd5e3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cd5e3-105">**Value**</span></span>|<span data-ttu-id="cd5e3-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cd5e3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd5e3-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="cd5e3-107">TRUE</span></span>  <br/> |<span data-ttu-id="cd5e3-108">O preenchimento de gradiente é exibido na forma.</span><span class="sxs-lookup"><span data-stu-id="cd5e3-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="cd5e3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="cd5e3-109">FALSE</span></span>  <br/> |<span data-ttu-id="cd5e3-110">Os preenchimentos de gradiente não são exibidos na forma.</span><span class="sxs-lookup"><span data-stu-id="cd5e3-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd5e3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd5e3-111">Remarks</span></span>

<span data-ttu-id="cd5e3-112">Para fazer referência à célula **FillGradientEnabled** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="cd5e3-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cd5e3-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cd5e3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="cd5e3-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="cd5e3-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="cd5e3-115">Para fazer referência à célula **FillGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cd5e3-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cd5e3-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cd5e3-116">Section index:</span></span>  <br/> |<span data-ttu-id="cd5e3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cd5e3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cd5e3-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cd5e3-118">Row index:</span></span>  <br/> |<span data-ttu-id="cd5e3-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="cd5e3-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="cd5e3-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="cd5e3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cd5e3-121">\*\*visFillGradientEnabled \*\*</span><span class="sxs-lookup"><span data-stu-id="cd5e3-121">\*\*visFillGradientEnabled \*\*</span></span> <br/> |
   

