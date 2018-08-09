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
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771499"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="f8cb0-103">Célula Color (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="f8cb0-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="f8cb0-104">Determina a cor utilizada no texto da forma.</span><span class="sxs-lookup"><span data-stu-id="f8cb0-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8cb0-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8cb0-105">Remarks</span></span>

<span data-ttu-id="f8cb0-106">Para definir a cor, insira um número de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="f8cb0-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="f8cb0-107">Para inserir uma cor personalizada, use a função RGB ou HSL.</span><span class="sxs-lookup"><span data-stu-id="f8cb0-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="f8cb0-108">O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f8cb0-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="f8cb0-109">Quando usado em operações numéricas, as cores têm valores de 24 e acima.</span><span class="sxs-lookup"><span data-stu-id="f8cb0-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="f8cb0-110">É possível definir a transparência da cor do texto na célula Transparency.</span><span class="sxs-lookup"><span data-stu-id="f8cb0-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="f8cb0-111">Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f8cb0-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8cb0-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f8cb0-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f8cb0-113">Char.Color [ *i* ] onde *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="f8cb0-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="f8cb0-114">Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f8cb0-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8cb0-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f8cb0-115">Section index:</span></span>  <br/> |<span data-ttu-id="f8cb0-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="f8cb0-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="f8cb0-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f8cb0-117">Row index:</span></span>  <br/> |<span data-ttu-id="f8cb0-118">**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="f8cb0-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="f8cb0-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f8cb0-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f8cb0-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="f8cb0-120">**visCharacterColor**</span></span> <br/> |
   

