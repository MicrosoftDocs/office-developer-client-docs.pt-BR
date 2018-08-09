---
title: Célula TextBkgnd (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Determina a cor do plano de fundo do texto de uma forma.
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773133"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="f1f96-103">Célula TextBkgnd (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="f1f96-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="f1f96-104">Determina a cor do plano de fundo do texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="f1f96-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1f96-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1f96-105">Remarks</span></span>

<span data-ttu-id="f1f96-106">A célula TextBkgnd pode ter qualquer valor de 0 a 24 ou 255.</span><span class="sxs-lookup"><span data-stu-id="f1f96-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="f1f96-107">Os valores 0 e 255 ( *visTxtBlklOpaque*) indicam um plano de fundo do texto transparente.</span><span class="sxs-lookup"><span data-stu-id="f1f96-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="f1f96-108">Para inserir uma cor personalizada, use a função RGB ou HSL mais um — por exemplo, RGB (255,127,255) + 1.</span><span class="sxs-lookup"><span data-stu-id="f1f96-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="f1f96-109">O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*) + 1, em vez de um número, será exibido na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f1f96-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="f1f96-110">Quando usado em operações numéricas, as cores têm valores de 25 e acima.</span><span class="sxs-lookup"><span data-stu-id="f1f96-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="f1f96-111">É possível definir a transparência da cor do plano de fundo do texto na célula TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="f1f96-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="f1f96-112">Para obter uma referência para a célula TextBkgnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f1f96-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1f96-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f1f96-113">Cell name:</span></span>  <br/> |<span data-ttu-id="f1f96-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="f1f96-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="f1f96-115">Para obter uma referência para a célula TextBkgnd pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f1f96-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1f96-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f1f96-116">Section index:</span></span>  <br/> |<span data-ttu-id="f1f96-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1f96-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f1f96-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f1f96-118">Row index:</span></span>  <br/> |<span data-ttu-id="f1f96-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="f1f96-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="f1f96-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f1f96-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f1f96-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="f1f96-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

