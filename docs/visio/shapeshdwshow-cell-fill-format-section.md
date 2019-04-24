---
title: Célula ShapeShdwShow (seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina se a forma exibe uma sombra, como um inteiro de 0 a 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349144"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="68190-103">Célula ShapeShdwShow (seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="68190-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="68190-104">Determina se a forma exibe uma sombra, como um inteiro de 0 a 2.</span><span class="sxs-lookup"><span data-stu-id="68190-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="68190-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="68190-105">**Value**</span></span>|<span data-ttu-id="68190-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68190-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68190-107">,0</span><span class="sxs-lookup"><span data-stu-id="68190-107">0</span></span>  <br/> |<span data-ttu-id="68190-108">Sempre exibe a sombra se for especificada uma sombra.</span><span class="sxs-lookup"><span data-stu-id="68190-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="68190-109">As sombras de subformas não são exibidas.</span><span class="sxs-lookup"><span data-stu-id="68190-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="68190-110">1</span><span class="sxs-lookup"><span data-stu-id="68190-110">1</span></span>  <br/> |<span data-ttu-id="68190-111">Não processa uma sombra, a menos que a forma não tenha um pai.</span><span class="sxs-lookup"><span data-stu-id="68190-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="68190-112">Use as sombras de subformas, se agrupadas.</span><span class="sxs-lookup"><span data-stu-id="68190-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="68190-113">duas</span><span class="sxs-lookup"><span data-stu-id="68190-113">2</span></span>  <br/> |<span data-ttu-id="68190-114">Sempre exibe uma sombra se uma sombra é especificada.</span><span class="sxs-lookup"><span data-stu-id="68190-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="68190-115">As sombras das subformas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="68190-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68190-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="68190-116">Remarks</span></span>

<span data-ttu-id="68190-117">Para obter uma referência para a célula **ShapeShdwShow** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="68190-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68190-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="68190-118">Cell name:</span></span>  <br/> | <span data-ttu-id="68190-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="68190-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="68190-120">Para obter uma referência para a célula **ShapeShdwShow** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="68190-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68190-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="68190-121">Section index:</span></span>  <br/> |<span data-ttu-id="68190-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68190-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="68190-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="68190-123">Row index:</span></span>  <br/> |<span data-ttu-id="68190-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="68190-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="68190-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="68190-125">Cell index:</span></span>  <br/> |<span data-ttu-id="68190-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="68190-126">**visFillShdwShow**</span></span> <br/> |
   

