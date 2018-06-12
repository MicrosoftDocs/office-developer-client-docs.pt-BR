---
title: Célula Active (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Especifica se a camada está ativa. As formas sem camadas atribuídas previamente são atribuídas à(s) camada(s) ativa(s) quando você as arrasta para a página de desenho.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771250"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="a6f61-104">Célula Active (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="a6f61-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="a6f61-p102">Especifica se a camada está ativa. As formas sem camadas atribuídas previamente são atribuídas à(s) camada(s) ativa(s) quando você as arrasta para a página de desenho.</span><span class="sxs-lookup"><span data-stu-id="a6f61-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="a6f61-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a6f61-107">**Value**</span></span>|<span data-ttu-id="a6f61-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a6f61-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6f61-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="a6f61-109">TRUE</span></span>  <br/> |<span data-ttu-id="a6f61-110">A camada está ativa.</span><span class="sxs-lookup"><span data-stu-id="a6f61-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="a6f61-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="a6f61-111">FALSE</span></span>  <br/> |<span data-ttu-id="a6f61-112">A camada não está ativa.</span><span class="sxs-lookup"><span data-stu-id="a6f61-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6f61-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a6f61-113">Remarks</span></span>

<span data-ttu-id="a6f61-114">O valor desta célula corresponde à configuração **ativa** na caixa de diálogo **Propriedades da camada** (no grupo **edição** na guia **página inicial** , clique em **camadas**e, em seguida, clique em **Propriedades da camada**).</span><span class="sxs-lookup"><span data-stu-id="a6f61-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="a6f61-115">Para obter uma referência à célula Active pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="a6f61-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6f61-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a6f61-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a6f61-117">Layers.Active [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a6f61-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a6f61-118">Para obter uma referência à célula Active pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a6f61-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6f61-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a6f61-119">Section index:</span></span>  <br/> |<span data-ttu-id="a6f61-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="a6f61-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="a6f61-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a6f61-121">Row index:</span></span>  <br/> |<span data-ttu-id="a6f61-122">**visRowLayer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a6f61-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a6f61-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a6f61-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a6f61-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="a6f61-124">**visLayerActive**</span></span> <br/> |
   

