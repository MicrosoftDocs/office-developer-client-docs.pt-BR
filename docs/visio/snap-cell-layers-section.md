---
title: Célula Snap (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Determina se outras formas podem ser ajustadas a formas atribuídas à camada. Formas atribuídas à camada podem ser ajustadas a outras formas, mas o contrário não ocorre.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434841"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="4ebe7-104">Célula Snap (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="4ebe7-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="4ebe7-p102">Determina se outras formas podem ser ajustadas a formas atribuídas à camada. Formas atribuídas à camada podem ser ajustadas a outras formas, mas o contrário não ocorre.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="4ebe7-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-107">**Value**</span></span>|<span data-ttu-id="4ebe7-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ebe7-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="4ebe7-109">TRUE</span></span>  <br/> |<span data-ttu-id="4ebe7-110">Outras formas podem ser ajustadas a formas na camada.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="4ebe7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4ebe7-111">FALSE</span></span>  <br/> |<span data-ttu-id="4ebe7-112">Outras formas não podem ser ajustadas a formas na camada.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ebe7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ebe7-113">Remarks</span></span>

<span data-ttu-id="4ebe7-114">Também é possível definir o valor dessa célula usando a opção **Ajustar** na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial** no grupo **Edição** clique em **Camadas** e em **Propriedades da Camada**).</span><span class="sxs-lookup"><span data-stu-id="4ebe7-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="4ebe7-115">Para obter uma referência para a célula Snap pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4ebe7-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ebe7-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4ebe7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="4ebe7-117">Layers.Snap[ *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4ebe7-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4ebe7-118">Para obter uma referência para a célula Snap pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4ebe7-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ebe7-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4ebe7-119">Section index:</span></span>  <br/> |<span data-ttu-id="4ebe7-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="4ebe7-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="4ebe7-121">Row index:</span></span>  <br/> |<span data-ttu-id="4ebe7-122">**visRowLayer**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4ebe7-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4ebe7-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="4ebe7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4ebe7-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-124">**visLayerSnap**</span></span> <br/> |
   

