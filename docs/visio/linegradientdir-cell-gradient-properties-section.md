---
title: Célula LineGradientDir (seção Propriedades de gradiente)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina a direção do gradiente linha. Um gradiente pode ser linear, radial, retangular ou seguem um caminho.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772204"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="36af9-104">Célula LineGradientDir (seção Propriedades de gradiente)</span><span class="sxs-lookup"><span data-stu-id="36af9-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="36af9-105">Determina a direção do gradiente linha.</span><span class="sxs-lookup"><span data-stu-id="36af9-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="36af9-106">Um gradiente pode ser linear, radial, retangular ou seguem um caminho.</span><span class="sxs-lookup"><span data-stu-id="36af9-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="36af9-107">Um gradiente linear é o gradiente único que tem um valor de ângulo adicionais (conforme determinado pela célula **LineGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="36af9-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="36af9-108">Todas as outras direções gradientes têm predefinidas enumerações.</span><span class="sxs-lookup"><span data-stu-id="36af9-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="36af9-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="36af9-109">**Value**</span></span>|<span data-ttu-id="36af9-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36af9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36af9-111">0</span><span class="sxs-lookup"><span data-stu-id="36af9-111">0</span></span>  <br/> |<span data-ttu-id="36af9-112">Gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="36af9-112">Linear gradient.</span></span> <span data-ttu-id="36af9-113">A célula **LineGradientAngle** determina a direção do gradiente.</span><span class="sxs-lookup"><span data-stu-id="36af9-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="36af9-114">1 a 7</span><span class="sxs-lookup"><span data-stu-id="36af9-114">1-7</span></span>  <br/> |<span data-ttu-id="36af9-115">Gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="36af9-115">Radial gradients.</span></span> <span data-ttu-id="36af9-116">Gradiente estende para fora de um círculo de um ponto central.</span><span class="sxs-lookup"><span data-stu-id="36af9-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="36af9-117">8-12</span><span class="sxs-lookup"><span data-stu-id="36af9-117">8-12</span></span>  <br/> |<span data-ttu-id="36af9-118">Gradientes retangulares.</span><span class="sxs-lookup"><span data-stu-id="36af9-118">Rectangular gradients.</span></span> <span data-ttu-id="36af9-119">Estende o gradiente como uma linha direcional de uma origem com um esmaecer retangular.</span><span class="sxs-lookup"><span data-stu-id="36af9-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="36af9-120">13</span><span class="sxs-lookup"><span data-stu-id="36af9-120">13</span></span>  <br/> |<span data-ttu-id="36af9-121">Gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="36af9-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36af9-122">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="36af9-122">Remarks</span></span>

<span data-ttu-id="36af9-123">Para fazer referência à célula **LineGradientDir** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="36af9-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="36af9-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="36af9-124">Cell name:</span></span>  <br/> | <span data-ttu-id="36af9-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="36af9-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="36af9-126">Para obter uma referência à célula **LineGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="36af9-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="36af9-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="36af9-127">Section index:</span></span>  <br/> |<span data-ttu-id="36af9-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36af9-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="36af9-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="36af9-129">Row index:</span></span>  <br/> |<span data-ttu-id="36af9-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="36af9-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="36af9-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="36af9-131">Cell index:</span></span>  <br/> |<span data-ttu-id="36af9-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="36af9-132">**visLineGradientDir**</span></span> <br/> |
   

