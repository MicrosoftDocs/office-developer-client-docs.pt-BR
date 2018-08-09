---
title: Célula QuickStyleVariation (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina se devem ser substituídas as fórmulas e os valores de texto, linha e preenchimento cor (ou uma combinação dessas propriedades) usando cores que contraste com o plano de fundo do diagrama. O valor é um OR bit a bit 0, 1, 2, 4 e 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772632"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="cad42-104">Célula QuickStyleVariation (Seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="cad42-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="cad42-105">Determina se devem ser substituídas as fórmulas e os valores de texto, linha e preenchimento cor (ou uma combinação dessas propriedades) usando cores que contraste com o plano de fundo do diagrama.</span><span class="sxs-lookup"><span data-stu-id="cad42-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="cad42-106">O valor é um OR bit a bit 0, 1, 2, 4 e 8.</span><span class="sxs-lookup"><span data-stu-id="cad42-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="cad42-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cad42-107">**Value**</span></span>|<span data-ttu-id="cad42-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cad42-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cad42-109">0</span><span class="sxs-lookup"><span data-stu-id="cad42-109">0</span></span>  <br/> |<span data-ttu-id="cad42-110">Não altere o texto de uma forma, linha, ou preenchimento cor (ou qualquer combinação dessas propriedades) para permanecer visível contra a cor de plano de fundo determinado de um tema.</span><span class="sxs-lookup"><span data-stu-id="cad42-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="cad42-111">1</span><span class="sxs-lookup"><span data-stu-id="cad42-111">1</span></span>  <br/> |<span data-ttu-id="cad42-112">Não altere o texto de uma forma, linha, ou preenchimento cor (ou qualquer combinação dessas propriedades) para permanecer visível contra a cor de plano de fundo determinado de um tema.</span><span class="sxs-lookup"><span data-stu-id="cad42-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="cad42-113">2</span><span class="sxs-lookup"><span data-stu-id="cad42-113">2</span></span>  <br/> |<span data-ttu-id="cad42-114">Altere a cor do texto de uma forma, se necessário, permaneça visível contra um tema determinados cor de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="cad42-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="cad42-115">4</span><span class="sxs-lookup"><span data-stu-id="cad42-115">4</span></span>  <br/> |<span data-ttu-id="cad42-116">Altere a cor da linha de uma forma, se necessário, permaneça visível contra um tema determinados cor de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="cad42-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="cad42-117">8</span><span class="sxs-lookup"><span data-stu-id="cad42-117">8</span></span>  <br/> |<span data-ttu-id="cad42-118">Altere a cor de preenchimento de uma forma, se necessário, permaneça visível contra um tema determinados cor de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="cad42-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cad42-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cad42-119">Remarks</span></span>

<span data-ttu-id="cad42-120">Use a célula QuickStyleVariation para garantir a visibilidade em texto ou linhas quando estiverem fora qualquer geometria da forma visível (por exemplo, em uma forma cujo textbox é abaixo da parte inferior da forma, como aquelas nos diagramas de rede).</span><span class="sxs-lookup"><span data-stu-id="cad42-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="cad42-121">O valor da célula padrão é 0, o que significa que seu comportamento está inativo.</span><span class="sxs-lookup"><span data-stu-id="cad42-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="cad42-122">Qualquer outro valor dispara o comportamento da célula.</span><span class="sxs-lookup"><span data-stu-id="cad42-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="cad42-123">O valor de QuickStyleVariation substitui o valor produzido pela função THEMEVAL quando ele reside na cor (seção Character), FillForegnd ou LineColor células (ou geradas pelo referências diretas para essas três propriedades por meio de THEMEVAL (" CharacterColor"), THEMEVAL("FillColor") e THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="cad42-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="cad42-124">Para obter uma referência à célula **QuickStyleVariation** pelo nome, a partir de outra fórmula, fazendo com que o valor do atributo **N** de um elemento de **célula** ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cad42-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cad42-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cad42-125">Cell name:</span></span>  <br/> |<span data-ttu-id="cad42-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="cad42-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="cad42-127">Para obter uma referência à célula **QuickStyleVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cad42-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cad42-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cad42-128">Section index:</span></span>  <br/> |<span data-ttu-id="cad42-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cad42-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cad42-130">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cad42-130">Row index:</span></span>  <br/> |<span data-ttu-id="cad42-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="cad42-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="cad42-132">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cad42-132">Cell index:</span></span>  <br/> |<span data-ttu-id="cad42-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="cad42-133">**visQuickStyleVariation**</span></span> <br/> |
   

