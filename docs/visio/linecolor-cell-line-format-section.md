---
title: Célula LineColor (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Determina a cor da linha da forma.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416934"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="19961-103">Célula LineColor (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="19961-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="19961-104">Determina a cor da linha da forma.</span><span class="sxs-lookup"><span data-stu-id="19961-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19961-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="19961-105">Remarks</span></span>

<span data-ttu-id="19961-p101">Para definir a cor da linha, insira um número de 0 a 23, que serve como um índice para uma coleção de cores de linha. É possível visualizar a coleção de cores de linha na caixa de diálogo **Linha** (na guia **Página Inicial** no grupo **Forma**, clique em **Linha**, aponte para **Espessura** e clique em **Mais Linhas**). Você também pode definir o valor da célula LineColor na caixa de diálogo **Linha**).</span><span class="sxs-lookup"><span data-stu-id="19961-p101">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors. You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**). You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="19961-109">Para inserir uma cor personalizada, utilize a função RGB ou HSL.</span><span class="sxs-lookup"><span data-stu-id="19961-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="19961-110">O valor de uma cor personalizada é sua cor RGB, e RGB( *r, g, b*), em vez de um número, será mostrado na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="19961-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="19961-111">Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24.</span><span class="sxs-lookup"><span data-stu-id="19961-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="19961-112">É possível definir a transparência da cor de linha na célula LineColorTrans.</span><span class="sxs-lookup"><span data-stu-id="19961-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="19961-113">Para obter uma referência para a célula LineColor pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="19961-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19961-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="19961-114">Cell name:</span></span>  <br/> |<span data-ttu-id="19961-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="19961-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="19961-116">Para obter uma referência para a célula LineColor pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="19961-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19961-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="19961-117">Section index:</span></span>  <br/> |<span data-ttu-id="19961-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="19961-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="19961-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="19961-119">Row index:</span></span>  <br/> |<span data-ttu-id="19961-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="19961-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="19961-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="19961-121">Cell index:</span></span>  <br/> |<span data-ttu-id="19961-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="19961-122">**visLineColor**</span></span> <br/> |
   

