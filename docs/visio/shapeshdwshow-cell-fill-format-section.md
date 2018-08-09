---
title: Célula ShapeShdwShow (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772913"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="c8a72-103">Célula ShapeShdwShow (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="c8a72-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="c8a72-104">Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.</span><span class="sxs-lookup"><span data-stu-id="c8a72-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="c8a72-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c8a72-105">**Value**</span></span>|<span data-ttu-id="c8a72-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8a72-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8a72-107">0</span><span class="sxs-lookup"><span data-stu-id="c8a72-107">0</span></span>  <br/> |<span data-ttu-id="c8a72-108">Sempre exibe a sombra se uma sombra for especificada.</span><span class="sxs-lookup"><span data-stu-id="c8a72-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="c8a72-109">As sombras para subformas não são exibidas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="c8a72-110">1</span><span class="sxs-lookup"><span data-stu-id="c8a72-110">1</span></span>  <br/> |<span data-ttu-id="c8a72-111">Não processam uma sombra, a menos que a forma não tem um pai.</span><span class="sxs-lookup"><span data-stu-id="c8a72-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="c8a72-112">Use sombras de forma sub-recurso se agrupadas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="c8a72-113">2</span><span class="sxs-lookup"><span data-stu-id="c8a72-113">2</span></span>  <br/> |<span data-ttu-id="c8a72-114">Sempre exiba uma sombra se uma sombra for especificada.</span><span class="sxs-lookup"><span data-stu-id="c8a72-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="c8a72-115">As sombras para subformas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8a72-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8a72-116">Remarks</span></span>

<span data-ttu-id="c8a72-117">Para fazer referência à célula **ShapeShdwShow** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c8a72-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8a72-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c8a72-118">Cell name:</span></span>  <br/> | <span data-ttu-id="c8a72-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="c8a72-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="c8a72-120">Para obter uma referência à célula **ShapeShdwShow** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c8a72-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8a72-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c8a72-121">Section index:</span></span>  <br/> |<span data-ttu-id="c8a72-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8a72-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c8a72-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c8a72-123">Row index:</span></span>  <br/> |<span data-ttu-id="c8a72-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="c8a72-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="c8a72-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c8a72-125">Cell index:</span></span>  <br/> |<span data-ttu-id="c8a72-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="c8a72-126">**visFillShdwShow**</span></span> <br/> |
   

