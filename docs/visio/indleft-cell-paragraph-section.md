---
title: Célula IndLeft (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem esquerda do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo esquerdo será o mesmo.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772070"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="c3e57-105">Célula IndLeft (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="c3e57-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="c3e57-p102">Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem esquerda do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo esquerdo será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="c3e57-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3e57-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3e57-109">Remarks</span></span>

<span data-ttu-id="c3e57-110">Para fazer referência à célula IndLeft pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c3e57-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3e57-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c3e57-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c3e57-112">Para.IndLeft [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c3e57-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c3e57-113">Para fazer referência à célula IndLeft pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c3e57-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3e57-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c3e57-114">Section index:</span></span>  <br/> |<span data-ttu-id="c3e57-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c3e57-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c3e57-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c3e57-116">Row index:</span></span>  <br/> |<span data-ttu-id="c3e57-117">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c3e57-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c3e57-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c3e57-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c3e57-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="c3e57-119">**visIndentLeft**</span></span> <br/> |
   

