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
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335333"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="400be-105">Célula IndLeft (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="400be-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="400be-p102">Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem esquerda do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo esquerdo será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="400be-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="400be-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="400be-109">Remarks</span></span>

<span data-ttu-id="400be-110">Para fazer referência à célula IndLeft pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="400be-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="400be-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="400be-111">Cell name:</span></span>  <br/> | <span data-ttu-id="400be-112">Para. IndLeft [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="400be-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="400be-113">Para fazer referência à célula IndLeft pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="400be-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="400be-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="400be-114">Section index:</span></span>  <br/> |<span data-ttu-id="400be-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="400be-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="400be-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="400be-116">Row index:</span></span>  <br/> |<span data-ttu-id="400be-117">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="400be-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="400be-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="400be-118">Cell index:</span></span>  <br/> |<span data-ttu-id="400be-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="400be-119">**visIndentLeft**</span></span> <br/> |
   

