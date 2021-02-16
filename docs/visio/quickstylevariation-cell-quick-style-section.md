---
title: Célula QuickStyleVariation (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina se deve substituir as fórmulas e os valores de texto, linha e cor de preenchimento (ou uma combinação dessas propriedades) usando cores que contrastam com o plano de fundo do diagrama. O valor é um BIT OR de 0, 1, 2, 4 e 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433791"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="fd4b7-104">Célula QuickStyleVariation (Seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="fd4b7-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="fd4b7-105">Determina se deve substituir as fórmulas e os valores de texto, linha e cor de preenchimento (ou uma combinação dessas propriedades) usando cores que contrastam com o plano de fundo do diagrama.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="fd4b7-106">O valor é um BIT OR de 0, 1, 2, 4 e 8.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="fd4b7-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd4b7-107">**Value**</span></span>|<span data-ttu-id="fd4b7-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd4b7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd4b7-109">0</span><span class="sxs-lookup"><span data-stu-id="fd4b7-109">0</span></span>  <br/> |<span data-ttu-id="fd4b7-110">Não altere a cor de preenchimento, linha ou texto de uma forma (ou qualquer combinação dessas propriedades) para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fd4b7-111">1 </span><span class="sxs-lookup"><span data-stu-id="fd4b7-111">1</span></span>  <br/> |<span data-ttu-id="fd4b7-112">Não altere a cor de preenchimento, linha ou texto de uma forma (ou qualquer combinação dessas propriedades) para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fd4b7-113">2 </span><span class="sxs-lookup"><span data-stu-id="fd4b7-113">2</span></span>  <br/> |<span data-ttu-id="fd4b7-114">Altere a cor do texto de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fd4b7-115">4 </span><span class="sxs-lookup"><span data-stu-id="fd4b7-115">4</span></span>  <br/> |<span data-ttu-id="fd4b7-116">Altere a cor da linha de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="fd4b7-117">8 </span><span class="sxs-lookup"><span data-stu-id="fd4b7-117">8</span></span>  <br/> |<span data-ttu-id="fd4b7-118">Altere a cor de preenchimento de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd4b7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd4b7-119">Remarks</span></span>

<span data-ttu-id="fd4b7-120">Use a célula QuickStyleVariation para garantir a visibilidade em texto ou linhas quando elas estão fora de qualquer geometria de forma visível (por exemplo, em uma forma cuja caixa de texto está abaixo da parte inferior da forma, como aquelas em Diagramas de Rede).</span><span class="sxs-lookup"><span data-stu-id="fd4b7-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="fd4b7-121">O valor padrão da célula é 0, o que significa que seu comportamento está inativo.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="fd4b7-122">Qualquer outro valor aciona o comportamento da célula.</span><span class="sxs-lookup"><span data-stu-id="fd4b7-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="fd4b7-123">O valor QuickStyleVariation substitui o valor produzido pela função THEMEVAL quando reside nas células Color (Seção Character), FillForegnd ou LineColor (ou produzido por referências diretas a essas três propriedades por meio de THEMEVAL("CharacterColor"), THEMEVAL("FillColor") e THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="fd4b7-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="fd4b7-124">Para obter uma referência para a célula **QuickStyleVariation** pelo nome, a partir de outra fórmula, ao obter o valor do atributo **N** de um elemento **Cell** ou de um programa usando a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="fd4b7-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd4b7-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fd4b7-125">Cell name:</span></span>  <br/> |<span data-ttu-id="fd4b7-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="fd4b7-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="fd4b7-127">Para fazer referência à **célula QuickStyleVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fd4b7-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd4b7-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fd4b7-128">Section index:</span></span>  <br/> |<span data-ttu-id="fd4b7-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd4b7-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fd4b7-130">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fd4b7-130">Row index:</span></span>  <br/> |<span data-ttu-id="fd4b7-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="fd4b7-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="fd4b7-132">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="fd4b7-132">Cell index:</span></span>  <br/> |<span data-ttu-id="fd4b7-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="fd4b7-133">**visQuickStyleVariation**</span></span> <br/> |
   

