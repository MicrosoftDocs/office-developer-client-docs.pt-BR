---
title: Célula Visible (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357810"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="d82a9-103">Célula Visible (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="d82a9-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="d82a9-104">Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="d82a9-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="d82a9-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d82a9-105">**Value**</span></span>|<span data-ttu-id="d82a9-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d82a9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d82a9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d82a9-107">TRUE</span></span>  <br/> |<span data-ttu-id="d82a9-108">As formas são visíveis.</span><span class="sxs-lookup"><span data-stu-id="d82a9-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="d82a9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d82a9-109">FALSE</span></span>  <br/> |<span data-ttu-id="d82a9-110">As formas estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="d82a9-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d82a9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d82a9-111">Remarks</span></span>

<span data-ttu-id="d82a9-112">Esta célula corresponde à opção **visível** na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e em Propriedades da **camada** ).</span><span class="sxs-lookup"><span data-stu-id="d82a9-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="d82a9-113">Para obter uma referência para a célula Visible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d82a9-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d82a9-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d82a9-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d82a9-115">Layers. Visible [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d82a9-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d82a9-116">Para obter uma referência para a célula Visible pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d82a9-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d82a9-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d82a9-117">Section index:</span></span>  <br/> |<span data-ttu-id="d82a9-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="d82a9-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="d82a9-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d82a9-119">Row index:</span></span>  <br/> |<span data-ttu-id="d82a9-120">**visRowLayer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d82a9-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d82a9-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d82a9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d82a9-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="d82a9-122">**visLayerVisible**</span></span> <br/> |
   

