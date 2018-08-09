---
title: Célula IndFirst (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Representa a distância do recuo da primeira linha de cada parágrafo no bloco de texto da forma em relação ao recuo esquerdo do parágrafo. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo da primeira linha será o mesmo.
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772061"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="a2029-105">Célula IndFirst (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="a2029-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="a2029-p102">Representa a distância do recuo da primeira linha de cada parágrafo no bloco de texto da forma em relação ao recuo esquerdo do parágrafo. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo da primeira linha será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="a2029-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2029-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2029-109">Remarks</span></span>

<span data-ttu-id="a2029-110">Para fazer referência à célula IndFirst pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a2029-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2029-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a2029-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a2029-112">Para.IndFirst [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a2029-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a2029-113">Para fazer referência à célula IndFirst pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a2029-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2029-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a2029-114">Section index:</span></span>  <br/> |<span data-ttu-id="a2029-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="a2029-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="a2029-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a2029-116">Row index:</span></span>  <br/> |<span data-ttu-id="a2029-117">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a2029-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a2029-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a2029-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a2029-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="a2029-119">**visIndentFirst**</span></span> <br/> |
   

