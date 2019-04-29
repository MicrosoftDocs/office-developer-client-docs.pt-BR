---
title: Célula TextPosAfterBullet (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Representa a distância entre a primeira linha do parágrafo e o marcador.
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422149"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="2a8cf-103">Célula TextPosAfterBullet (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="2a8cf-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="2a8cf-104">Representa a distância entre a primeira linha do parágrafo e o marcador.</span><span class="sxs-lookup"><span data-stu-id="2a8cf-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2a8cf-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a8cf-105">Remarks</span></span>

<span data-ttu-id="2a8cf-p101">A distância é adicionada à distância contida na célula IndFirst, que é o recuo esquerdo padrão. Esse valor não depende da escala do desenho.</span><span class="sxs-lookup"><span data-stu-id="2a8cf-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="2a8cf-108">Para fazer referência à célula TextPosAfterBullet pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2a8cf-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a8cf-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2a8cf-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2a8cf-110">Para. TextPosAfterBullet [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2a8cf-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2a8cf-111">Para fazer referência à célula TextPosAfterBullet pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2a8cf-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a8cf-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2a8cf-112">Section index:</span></span>  <br/> |<span data-ttu-id="2a8cf-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="2a8cf-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="2a8cf-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="2a8cf-114">Row index:</span></span>  <br/> |<span data-ttu-id="2a8cf-115">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2a8cf-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2a8cf-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2a8cf-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2a8cf-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="2a8cf-117">**visTextPosAfterBullet**</span></span> <br/> |
   

