---
title: Célula QuickStyleType (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina o tipo de Estilo Rápido (bidimensional, unidimensional ou conector) que a forma herda.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410501"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="fb587-103">Célula QuickStyleType (Seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="fb587-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="fb587-104">Determina o tipo de Estilo Rápido (bidimensional, unidimensional ou conector) que a forma herda.</span><span class="sxs-lookup"><span data-stu-id="fb587-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="fb587-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fb587-105">**Value**</span></span>|<span data-ttu-id="fb587-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fb587-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb587-107">0</span><span class="sxs-lookup"><span data-stu-id="fb587-107">0</span></span>  <br/> |<span data-ttu-id="fb587-108">O Visio escolhe automaticamente</span><span class="sxs-lookup"><span data-stu-id="fb587-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="fb587-109">1 </span><span class="sxs-lookup"><span data-stu-id="fb587-109">1</span></span>  <br/> |<span data-ttu-id="fb587-110">Unidimensional</span><span class="sxs-lookup"><span data-stu-id="fb587-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="fb587-111">2 </span><span class="sxs-lookup"><span data-stu-id="fb587-111">2</span></span>  <br/> |<span data-ttu-id="fb587-112">Bidimensional</span><span class="sxs-lookup"><span data-stu-id="fb587-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="fb587-113">3 </span><span class="sxs-lookup"><span data-stu-id="fb587-113">3</span></span>  <br/> |<span data-ttu-id="fb587-114">Connector</span><span class="sxs-lookup"><span data-stu-id="fb587-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb587-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb587-115">Remarks</span></span>

<span data-ttu-id="fb587-116">Para fazer referência à célula **QuickStyleType** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="fb587-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb587-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fb587-117">Cell name:</span></span>  <br/> | <span data-ttu-id="fb587-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="fb587-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="fb587-119">Para fazer referência à **célula QuickStyleType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fb587-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb587-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fb587-120">Section index:</span></span>  <br/> |<span data-ttu-id="fb587-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb587-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb587-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fb587-122">Row index:</span></span>  <br/> |<span data-ttu-id="fb587-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="fb587-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="fb587-124">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="fb587-124">Cell index:</span></span>  <br/> |<span data-ttu-id="fb587-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="fb587-125">**visQuickStyleType**</span></span> <br/> |
   

