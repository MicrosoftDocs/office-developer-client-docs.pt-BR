---
title: Célula FillBkgnd (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Determina a cor utilizada para o plano de fundo (preenchimento) do padrão de preenchimento da forma.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322509"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="f6eba-103">Célula FillBkgnd (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="f6eba-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="f6eba-104">Determina a cor utilizada para o plano de fundo (preenchimento) do padrão de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="f6eba-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6eba-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6eba-105">Remarks</span></span>

<span data-ttu-id="f6eba-106">Para definir a cor, insira um número de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="f6eba-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="f6eba-p101">Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB, e é isso (*r, g, b*), e não um número, que será mostrado na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24.</span><span class="sxs-lookup"><span data-stu-id="f6eba-p101">To enter a custom color, use the RGB or HSL function. The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window. When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="f6eba-110">É possível definir a transparência de preenchimento do plano de fundo na célula FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="f6eba-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="f6eba-111">Para obter uma referência para a célula FillBkgnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f6eba-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6eba-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f6eba-112">Cell name:</span></span>  <br/> | <span data-ttu-id="f6eba-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="f6eba-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="f6eba-114">Para obter uma referência para a célula FillBkgnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f6eba-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6eba-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f6eba-115">Section index:</span></span>  <br/> |<span data-ttu-id="f6eba-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6eba-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f6eba-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f6eba-117">Row index:</span></span>  <br/> |<span data-ttu-id="f6eba-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f6eba-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="f6eba-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f6eba-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f6eba-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="f6eba-120">**visFillBkgnd**</span></span> <br/> |
   

