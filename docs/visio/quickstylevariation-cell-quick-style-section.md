---
title: Célula QuickStyleVariation (seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina se as fórmulas e os valores de texto, linha e cor de preenchimento devem ser substituídos (ou uma combinação dessas propriedades) usando as cores que contrastam com o plano de fundo do diagrama. O valor é um bit a bit ou de 0, 1, 2, 4 e 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433791"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="c9765-104">Célula QuickStyleVariation (seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="c9765-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="c9765-105">Determina se as fórmulas e os valores de texto, linha e cor de preenchimento devem ser substituídos (ou uma combinação dessas propriedades) usando as cores que contrastam com o plano de fundo do diagrama.</span><span class="sxs-lookup"><span data-stu-id="c9765-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="c9765-106">O valor é um bit a bit ou de 0, 1, 2, 4 e 8.</span><span class="sxs-lookup"><span data-stu-id="c9765-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="c9765-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c9765-107">**Value**</span></span>|<span data-ttu-id="c9765-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c9765-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9765-109">,0</span><span class="sxs-lookup"><span data-stu-id="c9765-109">0</span></span>  <br/> |<span data-ttu-id="c9765-110">Não altere o texto, a linha ou a cor de preenchimento de uma forma (ou qualquer combinação dessas propriedades) para permanecer visível em relação à cor de plano de fundo específica de um tema.</span><span class="sxs-lookup"><span data-stu-id="c9765-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c9765-111">1</span><span class="sxs-lookup"><span data-stu-id="c9765-111">1</span></span>  <br/> |<span data-ttu-id="c9765-112">Não altere o texto, a linha ou a cor de preenchimento de uma forma (ou qualquer combinação dessas propriedades) para permanecer visível em relação à cor de plano de fundo específica de um tema.</span><span class="sxs-lookup"><span data-stu-id="c9765-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c9765-113">duas</span><span class="sxs-lookup"><span data-stu-id="c9765-113">2</span></span>  <br/> |<span data-ttu-id="c9765-114">Alterar a cor do texto de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="c9765-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c9765-115">4 </span><span class="sxs-lookup"><span data-stu-id="c9765-115">4</span></span>  <br/> |<span data-ttu-id="c9765-116">Altera a cor da linha de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo dada de um tema.</span><span class="sxs-lookup"><span data-stu-id="c9765-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c9765-117">8 </span><span class="sxs-lookup"><span data-stu-id="c9765-117">8</span></span>  <br/> |<span data-ttu-id="c9765-118">Alterar a cor de preenchimento de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="c9765-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9765-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9765-119">Remarks</span></span>

<span data-ttu-id="c9765-120">Use a célula QuickStyleVariation para garantir visibilidade em texto ou nas linhas quando estiverem fora de qualquer geometria de forma visível (por exemplo, em uma forma cuja caixa de texto está abaixo da parte inferior da forma, como aquelas em diagramas de rede).</span><span class="sxs-lookup"><span data-stu-id="c9765-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="c9765-121">O valor padrão da célula é 0, o que significa que seu comportamento está inativo.</span><span class="sxs-lookup"><span data-stu-id="c9765-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="c9765-122">Qualquer outro valor dispara o comportamento da célula.</span><span class="sxs-lookup"><span data-stu-id="c9765-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="c9765-123">O valor QuickStyleVariation substitui o valor produzido pela função THEMEVAL ao residir nas células Color (seção Character), FillForegnd ou LineColor (ou produzida por referências diretas a essas três propriedades por meio de THEMEVAL (" CharacterColor "), THEMEVAL (" FillColor ") e THEMEVAL (" LineColor ")).</span><span class="sxs-lookup"><span data-stu-id="c9765-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="c9765-124">Para obter uma referência para a célula **QuickStyleVariation** pelo nome, a partir de outra fórmula, obter o valor do atributo **N** de um elemento **Cell** ou de um programa usando a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c9765-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9765-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c9765-125">Cell name:</span></span>  <br/> |<span data-ttu-id="c9765-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="c9765-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="c9765-127">Para obter uma referência para a célula **QuickStyleVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c9765-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9765-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c9765-128">Section index:</span></span>  <br/> |<span data-ttu-id="c9765-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9765-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c9765-130">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c9765-130">Row index:</span></span>  <br/> |<span data-ttu-id="c9765-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="c9765-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="c9765-132">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c9765-132">Cell index:</span></span>  <br/> |<span data-ttu-id="c9765-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="c9765-133">**visQuickStyleVariation**</span></span> <br/> |
   

