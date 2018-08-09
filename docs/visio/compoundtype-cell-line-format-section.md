---
title: Célula CompoundType (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina o tipo de compostos da linha de uma forma.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771546"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="94250-103">Célula CompoundType (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="94250-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="94250-104">Determina o tipo de compostos da linha de uma forma.</span><span class="sxs-lookup"><span data-stu-id="94250-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="94250-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="94250-105">**Value**</span></span>|<span data-ttu-id="94250-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="94250-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94250-107">0</span><span class="sxs-lookup"><span data-stu-id="94250-107">0</span></span>  <br/> |<span data-ttu-id="94250-108">Simples</span><span class="sxs-lookup"><span data-stu-id="94250-108">Simple</span></span>  <br/> |
|<span data-ttu-id="94250-109">1</span><span class="sxs-lookup"><span data-stu-id="94250-109">1</span></span>  <br/> |<span data-ttu-id="94250-110">Double</span><span class="sxs-lookup"><span data-stu-id="94250-110">Double</span></span>  <br/> |
|<span data-ttu-id="94250-111">2</span><span class="sxs-lookup"><span data-stu-id="94250-111">2</span></span>  <br/> |<span data-ttu-id="94250-112">Espessura finas</span><span class="sxs-lookup"><span data-stu-id="94250-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="94250-113">3</span><span class="sxs-lookup"><span data-stu-id="94250-113">3</span></span>  <br/> |<span data-ttu-id="94250-114">Grossa fina</span><span class="sxs-lookup"><span data-stu-id="94250-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="94250-115">4</span><span class="sxs-lookup"><span data-stu-id="94250-115">4</span></span>  <br/> |<span data-ttu-id="94250-116">Triple</span><span class="sxs-lookup"><span data-stu-id="94250-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94250-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="94250-117">Remarks</span></span>

<span data-ttu-id="94250-118">Para fazer referência à célula **CompoundType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="94250-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94250-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="94250-119">Cell name:</span></span>  <br/> | <span data-ttu-id="94250-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="94250-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="94250-121">Para obter uma referência à célula **CompoundType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="94250-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94250-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="94250-122">Section index:</span></span>  <br/> |<span data-ttu-id="94250-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94250-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="94250-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="94250-124">Row index:</span></span>  <br/> |<span data-ttu-id="94250-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="94250-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="94250-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="94250-126">Cell index:</span></span>  <br/> |<span data-ttu-id="94250-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="94250-127">**visCompoundType**</span></span> <br/> |
   

