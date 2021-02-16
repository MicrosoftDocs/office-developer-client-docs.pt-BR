---
title: Célula SpLine (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Determina a distância entre uma linha do texto e a próxima, expressa em porcentagem, sendo 100% a altura da linha de um texto.
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434911"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="396b6-103">Célula SpLine (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="396b6-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="396b6-104">Determina a distância entre uma linha do texto e a próxima, expressa em porcentagem, sendo 100% a altura da linha de um texto.</span><span class="sxs-lookup"><span data-stu-id="396b6-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="396b6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="396b6-105">**Value**</span></span>|<span data-ttu-id="396b6-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="396b6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="396b6-107">\>0</span><span class="sxs-lookup"><span data-stu-id="396b6-107">\>0</span></span>  <br/> | <span data-ttu-id="396b6-108">Espaçamento absoluto, independentemente do tamanho da fonte</span><span class="sxs-lookup"><span data-stu-id="396b6-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="396b6-109">=0</span><span class="sxs-lookup"><span data-stu-id="396b6-109">=0</span></span>  <br/> | <span data-ttu-id="396b6-110">Definir sólido (espaçamento = 100% do tamanho da fonte)</span><span class="sxs-lookup"><span data-stu-id="396b6-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="396b6-111">\<0</span><span class="sxs-lookup"><span data-stu-id="396b6-111">\<0</span></span>  <br/> | <span data-ttu-id="396b6-112">Uma porcentagem do tamanho da fonte (por exemplo, -120% produz 120% de espaçamento)</span><span class="sxs-lookup"><span data-stu-id="396b6-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="396b6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="396b6-113">Remarks</span></span>

<span data-ttu-id="396b6-114">Para fazer referência à célula SpLine pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="396b6-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="396b6-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="396b6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="396b6-116">Para.</span><span class="sxs-lookup"><span data-stu-id="396b6-116">Para.</span></span> <span data-ttu-id="396b6-117">SpLine [  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="396b6-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="396b6-118">Para fazer referência à célula SpLine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="396b6-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="396b6-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="396b6-119">Section index:</span></span>  <br/> |<span data-ttu-id="396b6-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="396b6-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="396b6-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="396b6-121">Row index:</span></span>  <br/> |<span data-ttu-id="396b6-122">**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="396b6-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="396b6-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="396b6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="396b6-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="396b6-124">**visSpaceLine**</span></span> <br/> |
   

