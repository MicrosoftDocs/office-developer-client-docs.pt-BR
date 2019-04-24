---
title: Célula BulletFont (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Representa o número da fonte usada para formatar o texto quando uma sequência de caracteres com marcadores personalizada for especificada e o valor da célula Bullet for diferente de zero.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337552"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="04c05-103">Célula BulletFont (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="04c05-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="04c05-104">Representa o número da fonte usada para formatar o texto quando uma sequência de caracteres com marcadores personalizada for especificada e o valor da célula Bullet for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="04c05-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04c05-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="04c05-105">Remarks</span></span>

<span data-ttu-id="04c05-p101">Os números de fonte variam de acordo com as fontes instaladas em seu sistema. Se o valor for 0 e houver uma sequência de caracteres com marcadores personalizada, a fonte usada será a mesma do primeiro caractere do parágrafo.</span><span class="sxs-lookup"><span data-stu-id="04c05-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="04c05-108">Para fazer referência à célula BulletFont pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="04c05-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04c05-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="04c05-109">Cell name:</span></span>  <br/> | <span data-ttu-id="04c05-110">Para. BulletFont [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="04c05-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="04c05-111">Para fazer referência à célula BulletFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="04c05-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04c05-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="04c05-112">Section index:</span></span>  <br/> |<span data-ttu-id="04c05-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="04c05-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="04c05-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="04c05-114">Row index:</span></span>  <br/> |<span data-ttu-id="04c05-115">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="04c05-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="04c05-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="04c05-116">Cell index:</span></span>  <br/> |<span data-ttu-id="04c05-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="04c05-117">**visBulletFont**</span></span> <br/> |
   

