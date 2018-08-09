---
title: Célula QuickStyleType (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina o tipo de estilos rápidos (dimensional-2, 1-dimensional, ou um conector) que herda a forma.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772629"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="5ae7c-103">Célula QuickStyleType (Seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="5ae7c-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="5ae7c-104">Determina o tipo de estilos rápidos (dimensional-2, 1-dimensional, ou um conector) que herda a forma.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="5ae7c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-105">**Value**</span></span>|<span data-ttu-id="5ae7c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ae7c-107">0</span><span class="sxs-lookup"><span data-stu-id="5ae7c-107">0</span></span>  <br/> |<span data-ttu-id="5ae7c-108">O Visio escolhe automaticamente</span><span class="sxs-lookup"><span data-stu-id="5ae7c-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="5ae7c-109">1</span><span class="sxs-lookup"><span data-stu-id="5ae7c-109">1</span></span>  <br/> |<span data-ttu-id="5ae7c-110">1-dimensional</span><span class="sxs-lookup"><span data-stu-id="5ae7c-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="5ae7c-111">2</span><span class="sxs-lookup"><span data-stu-id="5ae7c-111">2</span></span>  <br/> |<span data-ttu-id="5ae7c-112">2-dimensional</span><span class="sxs-lookup"><span data-stu-id="5ae7c-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="5ae7c-113">3</span><span class="sxs-lookup"><span data-stu-id="5ae7c-113">3</span></span>  <br/> |<span data-ttu-id="5ae7c-114">Conector</span><span class="sxs-lookup"><span data-stu-id="5ae7c-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ae7c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ae7c-115">Remarks</span></span>

<span data-ttu-id="5ae7c-116">Para fazer referência à célula **QuickStyleType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="5ae7c-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ae7c-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5ae7c-117">Cell name:</span></span>  <br/> | <span data-ttu-id="5ae7c-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="5ae7c-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="5ae7c-119">Para obter uma referência à célula **QuickStyleType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5ae7c-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ae7c-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5ae7c-120">Section index:</span></span>  <br/> |<span data-ttu-id="5ae7c-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ae7c-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5ae7c-122">Row index:</span></span>  <br/> |<span data-ttu-id="5ae7c-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="5ae7c-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5ae7c-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5ae7c-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-125">**visQuickStyleType**</span></span> <br/> |
   

