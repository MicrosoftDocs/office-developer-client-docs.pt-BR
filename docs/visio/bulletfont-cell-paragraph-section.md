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
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771442"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="86588-103">Célula BulletFont (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="86588-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="86588-104">Representa o número da fonte usada para formatar o texto quando uma sequência de caracteres com marcadores personalizada for especificada e o valor da célula Bullet for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="86588-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86588-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="86588-105">Remarks</span></span>

<span data-ttu-id="86588-p101">Os números de fonte variam de acordo com as fontes instaladas em seu sistema. Se o valor for 0 e houver uma sequência de caracteres com marcadores personalizada, a fonte usada será a mesma do primeiro caractere do parágrafo.</span><span class="sxs-lookup"><span data-stu-id="86588-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="86588-108">Para fazer referência à célula BulletFont pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="86588-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86588-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="86588-109">Cell name:</span></span>  <br/> | <span data-ttu-id="86588-110">Para.BulletFont [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="86588-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="86588-111">Para fazer referência à célula BulletFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="86588-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86588-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="86588-112">Section index:</span></span>  <br/> |<span data-ttu-id="86588-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="86588-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="86588-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="86588-114">Row index:</span></span>  <br/> |<span data-ttu-id="86588-115">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="86588-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="86588-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="86588-116">Cell index:</span></span>  <br/> |<span data-ttu-id="86588-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="86588-117">**visBulletFont**</span></span> <br/> |
   

