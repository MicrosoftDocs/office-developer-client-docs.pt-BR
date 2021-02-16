---
title: Célula Color (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Especifica a cor usada para exibir a camada.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435128"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="7a4aa-103">Célula Color (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="7a4aa-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="7a4aa-104">Especifica a cor usada para exibir a camada.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a4aa-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a4aa-105">Remarks</span></span>

<span data-ttu-id="7a4aa-106">Para definir a cor, insira um número de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="7a4aa-107">Esse valor de célula corresponde à  configuração de cor  camada na caixa de diálogo  Propriedades da camada (no grupo edição na guia Página Início, clique em Camadas e em Propriedades **da camada**).  </span><span class="sxs-lookup"><span data-stu-id="7a4aa-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="7a4aa-108">Para inserir uma cor personalizada, utilize a função RGB ou HSL.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="7a4aa-109">O valor de uma cor personalizada é sua cor RGB, e RGB( *r, g, b*), em vez de um número, será mostrado na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="7a4aa-110">Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="7a4aa-111">O valor 255 indica que a camada está sem cor.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="7a4aa-112">É possível definir a transparência da cor da camada na célula Transparency.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="7a4aa-113">Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7a4aa-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a4aa-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7a4aa-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7a4aa-115">Layers.Color[ *i*  ] onde i =  *<*  1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="7a4aa-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="7a4aa-116">Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7a4aa-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a4aa-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7a4aa-117">Section index:</span></span>  <br/> |<span data-ttu-id="7a4aa-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="7a4aa-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="7a4aa-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="7a4aa-119">Row index:</span></span>  <br/> |<span data-ttu-id="7a4aa-120">**visRowLayer**  +   *i* onde *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="7a4aa-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="7a4aa-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="7a4aa-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7a4aa-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="7a4aa-122">**visLayerColor**</span></span> <br/> |
   

