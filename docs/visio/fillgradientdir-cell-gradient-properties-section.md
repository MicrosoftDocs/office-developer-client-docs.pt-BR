---
title: Célula FillGradientDir (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina a direção do gradiente do preenchimento. Um gradiente pode ser linear, radial, retangular ou seguem um caminho.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771868"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="23331-104">Célula FillGradientDir (Seção Gradient Properties)</span><span class="sxs-lookup"><span data-stu-id="23331-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="23331-105">Determina a direção do gradiente do preenchimento.</span><span class="sxs-lookup"><span data-stu-id="23331-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="23331-106">Um gradiente pode ser linear, radial, retangular ou seguem um caminho.</span><span class="sxs-lookup"><span data-stu-id="23331-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="23331-107">Um gradiente linear é o gradiente único que tem um valor de ângulo adicionais (conforme determinado pela célula **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="23331-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="23331-108">Todas as outras direções gradientes têm predefinidas enumerações.</span><span class="sxs-lookup"><span data-stu-id="23331-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="23331-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="23331-109">**Value**</span></span>|<span data-ttu-id="23331-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23331-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23331-111">0</span><span class="sxs-lookup"><span data-stu-id="23331-111">0</span></span>  <br/> |<span data-ttu-id="23331-112">Gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="23331-112">Linear gradient.</span></span> <span data-ttu-id="23331-113">A célula **FillGradientAngle** determina a direção do gradiente.</span><span class="sxs-lookup"><span data-stu-id="23331-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="23331-114">1 a 7</span><span class="sxs-lookup"><span data-stu-id="23331-114">1-7</span></span>  <br/> |<span data-ttu-id="23331-115">Gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="23331-115">Radial gradients.</span></span> <span data-ttu-id="23331-116">Gradiente estende para fora de um círculo de um ponto central.</span><span class="sxs-lookup"><span data-stu-id="23331-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="23331-117">8-12</span><span class="sxs-lookup"><span data-stu-id="23331-117">8-12</span></span>  <br/> |<span data-ttu-id="23331-118">Gradientes retangulares.</span><span class="sxs-lookup"><span data-stu-id="23331-118">Rectangular gradients.</span></span> <span data-ttu-id="23331-119">Estende o gradiente como uma linha direcional de uma origem com um esmaecer retangular.</span><span class="sxs-lookup"><span data-stu-id="23331-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="23331-120">13</span><span class="sxs-lookup"><span data-stu-id="23331-120">13</span></span>  <br/> |<span data-ttu-id="23331-121">Gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="23331-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23331-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="23331-122">Remarks</span></span>

<span data-ttu-id="23331-123">Para fazer referência à célula **FillGradientDir** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="23331-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23331-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="23331-124">Cell name:</span></span>  <br/> | <span data-ttu-id="23331-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="23331-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="23331-126">Para obter uma referência à célula **FillGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="23331-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23331-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="23331-127">Section index:</span></span>  <br/> |<span data-ttu-id="23331-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23331-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="23331-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="23331-129">Row index:</span></span>  <br/> |<span data-ttu-id="23331-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="23331-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="23331-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="23331-131">Cell index:</span></span>  <br/> |<span data-ttu-id="23331-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="23331-132">**visFillGradientDir**</span></span> <br/> |
   

