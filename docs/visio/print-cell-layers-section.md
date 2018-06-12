---
title: Célula Print (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Especifica se as formas pertencentes à camada podem ser impressas.
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772598"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="6b17d-103">Célula Print (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="6b17d-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="6b17d-104">Especifica se as formas pertencentes à camada podem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="6b17d-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="6b17d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6b17d-105">**Value**</span></span>|<span data-ttu-id="6b17d-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b17d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b17d-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="6b17d-107">TRUE</span></span>  <br/> |<span data-ttu-id="6b17d-108">As formas podem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="6b17d-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="6b17d-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="6b17d-109">FALSE</span></span>  <br/> |<span data-ttu-id="6b17d-110">As formas não podem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="6b17d-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b17d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b17d-111">Remarks</span></span>

<span data-ttu-id="6b17d-112">Você também pode definir esse valor usando a opção **Imprimir** na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e, em seguida, clique em **Propriedades da camada**).</span><span class="sxs-lookup"><span data-stu-id="6b17d-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="6b17d-113">Para obter uma referência para a célula Print pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="6b17d-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b17d-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6b17d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="6b17d-115">Layers.Print [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6b17d-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6b17d-116">Para obter uma referência para a célula Print pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6b17d-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b17d-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6b17d-117">Section index:</span></span>  <br/> |<span data-ttu-id="6b17d-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="6b17d-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="6b17d-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6b17d-119">Row index:</span></span>  <br/> |<span data-ttu-id="6b17d-120">**visRowLayer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6b17d-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6b17d-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6b17d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="6b17d-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="6b17d-122">**visDocPreviewScope**</span></span> <br/> |
   

