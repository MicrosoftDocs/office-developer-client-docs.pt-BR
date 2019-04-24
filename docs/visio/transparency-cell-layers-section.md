---
title: Célula Transparency (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Determina o nível de transparência para uma camada de cor.
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280949"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="11cd0-103">Célula Transparency (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="11cd0-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="11cd0-104">Determina o nível de transparência para uma camada de cor.</span><span class="sxs-lookup"><span data-stu-id="11cd0-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="11cd0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="11cd0-105">**Value**</span></span>|<span data-ttu-id="11cd0-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="11cd0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11cd0-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="11cd0-107">0 - 100</span></span>  <br/> |<span data-ttu-id="11cd0-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="11cd0-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11cd0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="11cd0-110">Remarks</span></span>

<span data-ttu-id="11cd0-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma camada com cor completamente transparente tenha a mesma aparência de uma camada sem cor na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%. Também é possível definir esse valor usando o controle deslizante na caixa de diálogo **Propriedades da Camada** (na guia \*\*Página Inicial \*\*, do grupo **Edição**, clique em **Camadas** e em **Propriedades da Camada**).</span><span class="sxs-lookup"><span data-stu-id="11cd0-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="11cd0-115">Para obter uma referência para a célula Transparency pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="11cd0-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11cd0-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="11cd0-116">Cell name:</span></span>  <br/> |<span data-ttu-id="11cd0-117">Layers. ColorTrans [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="11cd0-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="11cd0-118">Para obter uma referência para a célula Transparency pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="11cd0-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11cd0-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="11cd0-119">Section index:</span></span>  <br/> |<span data-ttu-id="11cd0-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="11cd0-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="11cd0-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="11cd0-121">Row index:</span></span>  <br/> |<span data-ttu-id="11cd0-122">**visRowLayer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="11cd0-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="11cd0-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="11cd0-123">Cell index:</span></span>  <br/> |<span data-ttu-id="11cd0-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="11cd0-124">**visLayerColorTrans**</span></span> <br/> |
   

