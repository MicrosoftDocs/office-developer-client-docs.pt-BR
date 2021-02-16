---
title: Célula NoLiveDynamics (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Determina se uma forma é redimensionada ou girada dinamicamente à medida que é manipulada.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421477"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="5a609-103">Célula NoLiveDynamics (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="5a609-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5a609-104">Determina se uma forma é redimensionada ou girada dinamicamente à medida que é manipulada.</span><span class="sxs-lookup"><span data-stu-id="5a609-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="5a609-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5a609-105">**Value**</span></span>|<span data-ttu-id="5a609-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a609-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5a609-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="5a609-107">TRUE</span></span>  <br/> | <span data-ttu-id="5a609-108">Não atualizar dinamicamente a forma à medida que é manipulada.</span><span class="sxs-lookup"><span data-stu-id="5a609-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="5a609-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5a609-109">FALSE</span></span>  <br/> | <span data-ttu-id="5a609-110">Atualizar dinamicamente a forma à medida que é manipulada.</span><span class="sxs-lookup"><span data-stu-id="5a609-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a609-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a609-111">Remarks</span></span>

<span data-ttu-id="5a609-p101">À medida que uma forma bidimensional (2D) é redimensionada ou girada sem a dinâmica ao vivo, é possível visualizar uma caixa de seleção. Se a forma for unidimensional (1D), o comentário visual terá como base o valor da célula DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="5a609-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="5a609-114">Para fazer referência à célula NoLiveDynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="5a609-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a609-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5a609-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5a609-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="5a609-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="5a609-117">Para fazer referência à célula NoLiveDynamics pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5a609-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a609-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5a609-118">Section index:</span></span>  <br/> |<span data-ttu-id="5a609-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5a609-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5a609-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="5a609-120">Row index:</span></span>  <br/> |<span data-ttu-id="5a609-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5a609-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="5a609-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="5a609-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5a609-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="5a609-123">**visNoLiveDynamics**</span></span> <br/> |
   

