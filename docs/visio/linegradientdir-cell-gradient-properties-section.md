---
title: Célula LineGradientDir (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina a direção do gradiente de linha. Um gradiente pode ser linear, radial, retangular ou seguir um caminho.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417984"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="ae3e0-104">Célula LineGradientDir (Seção Gradient Properties)</span><span class="sxs-lookup"><span data-stu-id="ae3e0-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="ae3e0-105">Determina a direção do gradiente de linha.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="ae3e0-106">Um gradiente pode ser linear, radial, retangular ou seguir um caminho.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ae3e0-107">Um gradiente linear é o único gradiente que recebe um valor de ângulo adicional (conforme determinado pela **célula LineGradientDir).**</span><span class="sxs-lookup"><span data-stu-id="ae3e0-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="ae3e0-108">Todas as outras direções de gradiente têm enumerações predefinidas.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="ae3e0-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae3e0-109">**Value**</span></span>|<span data-ttu-id="ae3e0-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae3e0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae3e0-111">0</span><span class="sxs-lookup"><span data-stu-id="ae3e0-111">0</span></span>  <br/> |<span data-ttu-id="ae3e0-112">Gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-112">Linear gradient.</span></span> <span data-ttu-id="ae3e0-113">A **célula LineGradientAngle** determina a direção do gradiente.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="ae3e0-114">1-7</span><span class="sxs-lookup"><span data-stu-id="ae3e0-114">1-7</span></span>  <br/> |<span data-ttu-id="ae3e0-115">Gradientes radiales.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-115">Radial gradients.</span></span> <span data-ttu-id="ae3e0-116">O gradiente se estende para fora em um círculo a partir de um ponto central.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="ae3e0-117">8-12</span><span class="sxs-lookup"><span data-stu-id="ae3e0-117">8-12</span></span>  <br/> |<span data-ttu-id="ae3e0-118">Gradientes retangulares.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-118">Rectangular gradients.</span></span> <span data-ttu-id="ae3e0-119">O gradiente se estende como uma linha direcional de uma origem com um fade em forma de retangular.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="ae3e0-120">13 </span><span class="sxs-lookup"><span data-stu-id="ae3e0-120">13</span></span>  <br/> |<span data-ttu-id="ae3e0-121">Gradiente do caminho.</span><span class="sxs-lookup"><span data-stu-id="ae3e0-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae3e0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae3e0-122">Remarks</span></span>

<span data-ttu-id="ae3e0-123">Para fazer referência à célula **LineGradientDir** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="ae3e0-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae3e0-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ae3e0-124">Cell name:</span></span>  <br/> | <span data-ttu-id="ae3e0-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="ae3e0-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="ae3e0-126">Para fazer referência à célula **LineGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ae3e0-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae3e0-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ae3e0-127">Section index:</span></span>  <br/> |<span data-ttu-id="ae3e0-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae3e0-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ae3e0-129">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ae3e0-129">Row index:</span></span>  <br/> |<span data-ttu-id="ae3e0-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="ae3e0-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="ae3e0-131">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="ae3e0-131">Cell index:</span></span>  <br/> |<span data-ttu-id="ae3e0-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="ae3e0-132">**visLineGradientDir**</span></span> <br/> |
   

