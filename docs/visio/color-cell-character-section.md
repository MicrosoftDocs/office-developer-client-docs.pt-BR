---
title: Célula Color (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Determina a cor utilizada no texto da forma.
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341836"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="8774f-103">Célula Color (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="8774f-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="8774f-104">Determina a cor utilizada no texto da forma.</span><span class="sxs-lookup"><span data-stu-id="8774f-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8774f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8774f-105">Remarks</span></span>

<span data-ttu-id="8774f-106">Para definir a cor, insira um número de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="8774f-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="8774f-107">Para inserir uma cor personalizada, utilize a função RGB ou HSL.</span><span class="sxs-lookup"><span data-stu-id="8774f-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="8774f-108">O valor de uma cor personalizada é sua cor RGB e RGB ( *r, g, b*), e não um número, serão mostrados na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8774f-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="8774f-109">Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24.</span><span class="sxs-lookup"><span data-stu-id="8774f-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="8774f-110">É possível definir a transparência da cor do texto na célula Transparency.</span><span class="sxs-lookup"><span data-stu-id="8774f-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="8774f-111">Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8774f-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8774f-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8774f-112">Cell name:</span></span>  <br/> |<span data-ttu-id="8774f-113">Char. Color [ *i* ] onde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="8774f-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="8774f-114">Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8774f-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8774f-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8774f-115">Section index:</span></span>  <br/> |<span data-ttu-id="8774f-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8774f-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="8774f-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8774f-117">Row index:</span></span>  <br/> |<span data-ttu-id="8774f-118">**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="8774f-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="8774f-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8774f-119">Cell index:</span></span>  <br/> |<span data-ttu-id="8774f-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="8774f-120">**visCharacterColor**</span></span> <br/> |
   

