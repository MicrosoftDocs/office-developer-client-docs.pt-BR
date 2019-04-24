---
title: Célula QuickStyleType (seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina o tipo de estilo rápido (bidimensional, 1-dimensional ou conector) que a forma herda.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282576"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="cd38e-103">Célula QuickStyleType (seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="cd38e-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="cd38e-104">Determina o tipo de estilo rápido (bidimensional, 1-dimensional ou conector) que a forma herda.</span><span class="sxs-lookup"><span data-stu-id="cd38e-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="cd38e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cd38e-105">**Value**</span></span>|<span data-ttu-id="cd38e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cd38e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd38e-107">,0</span><span class="sxs-lookup"><span data-stu-id="cd38e-107">0</span></span>  <br/> |<span data-ttu-id="cd38e-108">O Visio escolhe automaticamente</span><span class="sxs-lookup"><span data-stu-id="cd38e-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="cd38e-109">1</span><span class="sxs-lookup"><span data-stu-id="cd38e-109">1</span></span>  <br/> |<span data-ttu-id="cd38e-110">unidimensional</span><span class="sxs-lookup"><span data-stu-id="cd38e-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="cd38e-111">duas</span><span class="sxs-lookup"><span data-stu-id="cd38e-111">2</span></span>  <br/> |<span data-ttu-id="cd38e-112">bidimensionais</span><span class="sxs-lookup"><span data-stu-id="cd38e-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="cd38e-113">3D</span><span class="sxs-lookup"><span data-stu-id="cd38e-113">3</span></span>  <br/> |<span data-ttu-id="cd38e-114">Conector</span><span class="sxs-lookup"><span data-stu-id="cd38e-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd38e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd38e-115">Remarks</span></span>

<span data-ttu-id="cd38e-116">Para obter uma referência para a célula **QuickStyleType** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cd38e-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cd38e-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cd38e-117">Cell name:</span></span>  <br/> | <span data-ttu-id="cd38e-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="cd38e-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="cd38e-119">Para obter uma referência para a célula **QuickStyleType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cd38e-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cd38e-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cd38e-120">Section index:</span></span>  <br/> |<span data-ttu-id="cd38e-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cd38e-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cd38e-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cd38e-122">Row index:</span></span>  <br/> |<span data-ttu-id="cd38e-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="cd38e-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="cd38e-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cd38e-124">Cell index:</span></span>  <br/> |<span data-ttu-id="cd38e-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="cd38e-125">**visQuickStyleType**</span></span> <br/> |
   

