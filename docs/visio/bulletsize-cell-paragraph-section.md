---
title: Célula BulletSize (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Especifica o tamanho de um marcador.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337608"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="c0a40-103">Célula BulletSize (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="c0a40-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="c0a40-104">Especifica o tamanho de um marcador.</span><span class="sxs-lookup"><span data-stu-id="c0a40-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0a40-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0a40-105">Remarks</span></span>

<span data-ttu-id="c0a40-106">Esse valor pode ser especificado para marcadores predefinidos ou personalizados, como um valor percentual ou específico.</span><span class="sxs-lookup"><span data-stu-id="c0a40-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="c0a40-107">Se o valor for zero (0), o marcador terá o mesmo tamanho de fonte do primeiro caractere do parágrafo.</span><span class="sxs-lookup"><span data-stu-id="c0a40-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="c0a40-108">Se o valor for percentual, o tamanho do marcador será um percentual do tamanho da fonte do primeiro caractere do parágrafo.</span><span class="sxs-lookup"><span data-stu-id="c0a40-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="c0a40-109">Números negativos são tratados como percentuais.</span><span class="sxs-lookup"><span data-stu-id="c0a40-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="c0a40-110">Para fazer referência à célula BulletSize pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c0a40-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0a40-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c0a40-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c0a40-112">Para. BulletFontSize [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c0a40-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c0a40-113">Para fazer referência à célula BulletSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c0a40-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0a40-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c0a40-114">Section index:</span></span>  <br/> |<span data-ttu-id="c0a40-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c0a40-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c0a40-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c0a40-116">Row index:</span></span>  <br/> |<span data-ttu-id="c0a40-117">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c0a40-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c0a40-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c0a40-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c0a40-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="c0a40-119">**visBulletFontSize**</span></span> <br/> |
   

