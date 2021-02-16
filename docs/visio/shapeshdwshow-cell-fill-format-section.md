---
title: Célula ShapeShdwShow (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422114"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="d4445-103">Célula ShapeShdwShow (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="d4445-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="d4445-104">Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.</span><span class="sxs-lookup"><span data-stu-id="d4445-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="d4445-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d4445-105">**Value**</span></span>|<span data-ttu-id="d4445-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d4445-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4445-107">0</span><span class="sxs-lookup"><span data-stu-id="d4445-107">0</span></span>  <br/> |<span data-ttu-id="d4445-108">Sempre exibir a sombra se uma sombra for especificada.</span><span class="sxs-lookup"><span data-stu-id="d4445-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="d4445-109">As sombras de sub formas não são exibidas.</span><span class="sxs-lookup"><span data-stu-id="d4445-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="d4445-110">1 </span><span class="sxs-lookup"><span data-stu-id="d4445-110">1</span></span>  <br/> |<span data-ttu-id="d4445-111">Não renderizar uma sombra, a menos que a forma não tenha um pai.</span><span class="sxs-lookup"><span data-stu-id="d4445-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="d4445-112">Use sombras de sub shape se agrupadas.</span><span class="sxs-lookup"><span data-stu-id="d4445-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="d4445-113">2 </span><span class="sxs-lookup"><span data-stu-id="d4445-113">2</span></span>  <br/> |<span data-ttu-id="d4445-114">Sempre exibirá uma sombra se uma sombra for especificada.</span><span class="sxs-lookup"><span data-stu-id="d4445-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="d4445-115">As sombras de sub formas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="d4445-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4445-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4445-116">Remarks</span></span>

<span data-ttu-id="d4445-117">Para fazer referência à célula **ShapeShdwShow** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="d4445-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4445-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d4445-118">Cell name:</span></span>  <br/> | <span data-ttu-id="d4445-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="d4445-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="d4445-120">Para fazer referência à **célula ShapeShdwShow** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d4445-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4445-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d4445-121">Section index:</span></span>  <br/> |<span data-ttu-id="d4445-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4445-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d4445-123">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="d4445-123">Row index:</span></span>  <br/> |<span data-ttu-id="d4445-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d4445-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="d4445-125">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="d4445-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d4445-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="d4445-126">**visFillShdwShow**</span></span> <br/> |
   

