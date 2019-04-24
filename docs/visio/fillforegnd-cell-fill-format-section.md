---
title: Célula FillForegnd (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Determina a cor usada para o primeiro plano (traço) do padrão de preenchimento da forma.
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322502"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="d5652-103">Célula FillForegnd (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="d5652-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="d5652-104">Determina a cor usada para o primeiro plano (traço) do padrão de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="d5652-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5652-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5652-105">Remarks</span></span>

<span data-ttu-id="d5652-106">Para definir a cor, insira um número de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="d5652-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="d5652-107">Para inserir uma cor personalizada, utilize a função RGB ou HSL.</span><span class="sxs-lookup"><span data-stu-id="d5652-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="d5652-108">O valor de uma cor personalizada é sua cor RGB e RGB ( *r, g, b*), e não um número, serão mostrados na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d5652-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="d5652-109">Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24.</span><span class="sxs-lookup"><span data-stu-id="d5652-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="d5652-110">É possível definir a transparência de preenchimento do primeiro plano na célula FillForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="d5652-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="d5652-111">Para obter uma referência para a célula FillForegnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d5652-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5652-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d5652-112">Cell name:</span></span>  <br/> |<span data-ttu-id="d5652-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="d5652-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="d5652-114">Para obter uma referência para a célula FillForegnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d5652-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5652-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d5652-115">Section index:</span></span>  <br/> |<span data-ttu-id="d5652-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d5652-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d5652-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d5652-117">Row index:</span></span>  <br/> |<span data-ttu-id="d5652-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d5652-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="d5652-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d5652-119">Cell index:</span></span>  <br/> |<span data-ttu-id="d5652-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="d5652-120">**visFillForegnd**</span></span> <br/> |
   

