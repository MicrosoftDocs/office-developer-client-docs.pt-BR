---
title: Célula FillGradientDir (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina a direção do gradiente de preenchimento. Um gradiente pode ser linear, radial, retangular ou seguir um caminho.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322460"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="2a5e6-104">Célula FillGradientDir (seção Gradient Properties)</span><span class="sxs-lookup"><span data-stu-id="2a5e6-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="2a5e6-105">Determina a direção do gradiente de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="2a5e6-106">Um gradiente pode ser linear, radial, retangular ou seguir um caminho.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2a5e6-107">Um gradiente linear é o único gradiente que assume um valor de ângulo adicional (conforme determinado pela célula **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="2a5e6-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="2a5e6-108">Todas as outras direções de gradiente têm enumerações predefinidas.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="2a5e6-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2a5e6-109">**Value**</span></span>|<span data-ttu-id="2a5e6-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2a5e6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a5e6-111">,0</span><span class="sxs-lookup"><span data-stu-id="2a5e6-111">0</span></span>  <br/> |<span data-ttu-id="2a5e6-112">Gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-112">Linear gradient.</span></span> <span data-ttu-id="2a5e6-113">A célula **FillGradientAngle** determina a direção do gradiente.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="2a5e6-114">1-7</span><span class="sxs-lookup"><span data-stu-id="2a5e6-114">1-7</span></span>  <br/> |<span data-ttu-id="2a5e6-115">Gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-115">Radial gradients.</span></span> <span data-ttu-id="2a5e6-116">O gradiente se estende para cima em um círculo a partir de um ponto central.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="2a5e6-117">8-12</span><span class="sxs-lookup"><span data-stu-id="2a5e6-117">8-12</span></span>  <br/> |<span data-ttu-id="2a5e6-118">Gradientes retangulares.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-118">Rectangular gradients.</span></span> <span data-ttu-id="2a5e6-119">O gradiente estende-se como uma linha direcional de uma origem com um esmaecimento de forma retangular.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="2a5e6-120">Treze</span><span class="sxs-lookup"><span data-stu-id="2a5e6-120">13</span></span>  <br/> |<span data-ttu-id="2a5e6-121">Gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="2a5e6-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a5e6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a5e6-122">Remarks</span></span>

<span data-ttu-id="2a5e6-123">Para obter uma referência para a célula **FillGradientDir** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="2a5e6-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a5e6-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2a5e6-124">Cell name:</span></span>  <br/> | <span data-ttu-id="2a5e6-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="2a5e6-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="2a5e6-126">Para obter uma referência para a célula **FillGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2a5e6-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a5e6-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2a5e6-127">Section index:</span></span>  <br/> |<span data-ttu-id="2a5e6-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2a5e6-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2a5e6-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2a5e6-129">Row index:</span></span>  <br/> |<span data-ttu-id="2a5e6-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="2a5e6-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="2a5e6-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2a5e6-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2a5e6-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="2a5e6-132">**visFillGradientDir**</span></span> <br/> |
   

