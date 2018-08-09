---
title: Célula Style (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Mostra a formatação de caracteres aplicada a um intervalo de texto no bloco de texto da forma.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773061"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="a79ec-103">Célula Style (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="a79ec-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="a79ec-104">Mostra a formatação de caracteres aplicada a um intervalo de texto no bloco de texto da forma.</span><span class="sxs-lookup"><span data-stu-id="a79ec-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="a79ec-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="a79ec-105">**Style**</span></span>|<span data-ttu-id="a79ec-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a79ec-106">**Value**</span></span>|<span data-ttu-id="a79ec-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="a79ec-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a79ec-108">Negrito</span><span class="sxs-lookup"><span data-stu-id="a79ec-108">Bold</span></span>  <br/> | <span data-ttu-id="a79ec-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="a79ec-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="a79ec-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="a79ec-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="a79ec-111">Itálico</span><span class="sxs-lookup"><span data-stu-id="a79ec-111">Italic</span></span>  <br/> | <span data-ttu-id="a79ec-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="a79ec-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="a79ec-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="a79ec-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="a79ec-114">Sublinhado</span><span class="sxs-lookup"><span data-stu-id="a79ec-114">Underline</span></span>  <br/> | <span data-ttu-id="a79ec-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="a79ec-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="a79ec-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="a79ec-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="a79ec-117">Caixa alta</span><span class="sxs-lookup"><span data-stu-id="a79ec-117">Small caps</span></span>  <br/> | <span data-ttu-id="a79ec-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="a79ec-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="a79ec-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="a79ec-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a79ec-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a79ec-120">Remarks</span></span>

<span data-ttu-id="a79ec-p101">A célula Style conterá informações de formatação aplicada a um subintervalo de texto de uma forma se a seção Characters contiver diversas linhas. Caso contrário, ela conterá informações de formatação para todo o texto da forma.</span><span class="sxs-lookup"><span data-stu-id="a79ec-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="a79ec-123">O valor representa um número binário em que cada bit indica um estilo de caractere.</span><span class="sxs-lookup"><span data-stu-id="a79ec-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="a79ec-124">Por exemplo, um valor de 3 representa o texto formatado em itálico e negrito.</span><span class="sxs-lookup"><span data-stu-id="a79ec-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="a79ec-125">Se o valor do estilo for 0, o texto é simples ou não formatado.</span><span class="sxs-lookup"><span data-stu-id="a79ec-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="a79ec-126">Você pode testar para um determinado formato utilizando Boolean BIT\* funções.</span><span class="sxs-lookup"><span data-stu-id="a79ec-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="a79ec-127">Consulte a documentação de programação para obter detalhes sobre essas funções.</span><span class="sxs-lookup"><span data-stu-id="a79ec-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="a79ec-128">Para fazer referência à célula Style pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a79ec-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a79ec-129">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a79ec-129">Cell name:</span></span>  <br/> | <span data-ttu-id="a79ec-130">Char.Style [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a79ec-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a79ec-131">Para fazer referência à célula Style pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a79ec-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a79ec-132">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a79ec-132">Section index:</span></span>  <br/> |<span data-ttu-id="a79ec-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a79ec-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="a79ec-134">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a79ec-134">Row index:</span></span>  <br/> |<span data-ttu-id="a79ec-135">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a79ec-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a79ec-136">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a79ec-136">Cell index:</span></span>  <br/> |<span data-ttu-id="a79ec-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="a79ec-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="a79ec-138">*Exemplo*</span><span class="sxs-lookup"><span data-stu-id="a79ec-138">*Example*</span></span> 
  
<span data-ttu-id="a79ec-139">Suponha que a célula Color na primeira linha da seção Character de uma forma esteja definida para esta fórmula:</span><span class="sxs-lookup"><span data-stu-id="a79ec-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="a79ec-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="a79ec-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="a79ec-p103">Então, se o primeiro caractere do texto da forma for negrito, o texto abrangido pela primeira linha de propriedades da seção Character será azul (4); caso contrário, ele será verde (3). Esse exemplo supõe que as cores padrão estejam sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="a79ec-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="a79ec-p104">O exemplo a seguir ilustra como definir a célula Style em um programa. A primeira instrução faz referência à célula Style pelo nome, enquanto a segunda instrução faz referência pelo índice. As duas instruções aplicam o estilo itálico ao texto coberto pela segunda linha da seção Character de uma forma.</span><span class="sxs-lookup"><span data-stu-id="a79ec-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  
