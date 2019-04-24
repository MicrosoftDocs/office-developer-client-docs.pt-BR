---
title: Célula IndRight (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem direita do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo direito será o mesmo.
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335340"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="da07b-105">Célula IndRight (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="da07b-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="da07b-p102">Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem direita do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo direito será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="da07b-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da07b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="da07b-109">Remarks</span></span>

<span data-ttu-id="da07b-110">Para fazer referência à célula IndRight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="da07b-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="da07b-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="da07b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="da07b-112">Para. IndRight [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="da07b-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="da07b-113">Para fazer referência à célula IndRight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="da07b-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="da07b-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="da07b-114">Section index:</span></span>  <br/> |<span data-ttu-id="da07b-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="da07b-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="da07b-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="da07b-116">Row index:</span></span>  <br/> |<span data-ttu-id="da07b-117">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="da07b-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="da07b-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="da07b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="da07b-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="da07b-119">**visIndentRight**</span></span> <br/> |
   

