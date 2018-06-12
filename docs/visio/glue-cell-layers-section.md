---
title: Célula Glue (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Especifica se as formas pertencentes à camada podem ser coladas.
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771963"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="361d5-103">Célula Glue (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="361d5-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="361d5-104">Especifica se as formas pertencentes à camada podem ser coladas.</span><span class="sxs-lookup"><span data-stu-id="361d5-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="361d5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="361d5-105">**Value**</span></span>|<span data-ttu-id="361d5-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="361d5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="361d5-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="361d5-107">TRUE</span></span>  <br/> |<span data-ttu-id="361d5-108">A cola está ativada.</span><span class="sxs-lookup"><span data-stu-id="361d5-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="361d5-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="361d5-109">FALSE</span></span>  <br/> |<span data-ttu-id="361d5-110">A cola não está ativada.</span><span class="sxs-lookup"><span data-stu-id="361d5-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="361d5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="361d5-111">Remarks</span></span>

<span data-ttu-id="361d5-112">Essa célula corresponde à opção **associar** na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e, em seguida, clique em **Propriedades da camada** ).</span><span class="sxs-lookup"><span data-stu-id="361d5-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="361d5-113">Para fazer referência à célula Glue pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="361d5-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="361d5-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="361d5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="361d5-115">Layers.Glue [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="361d5-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="361d5-116">Para obter uma referência à célula Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="361d5-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="361d5-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="361d5-117">Section index:</span></span>  <br/> |<span data-ttu-id="361d5-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="361d5-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="361d5-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="361d5-119">Row index:</span></span>  <br/> |<span data-ttu-id="361d5-120">**visRowLayer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="361d5-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="361d5-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="361d5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="361d5-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="361d5-122">**visLayerGlue**</span></span> <br/> |
   

