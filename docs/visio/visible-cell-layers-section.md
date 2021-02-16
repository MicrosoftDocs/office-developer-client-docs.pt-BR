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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405447"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="7f51a-103">Célula Visible (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="7f51a-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="7f51a-104">Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="7f51a-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="7f51a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7f51a-105">**Value**</span></span>|<span data-ttu-id="7f51a-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7f51a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f51a-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="7f51a-107">TRUE</span></span>  <br/> |<span data-ttu-id="7f51a-108">As formas são visíveis.</span><span class="sxs-lookup"><span data-stu-id="7f51a-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="7f51a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7f51a-109">FALSE</span></span>  <br/> |<span data-ttu-id="7f51a-110">As formas estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="7f51a-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f51a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f51a-111">Remarks</span></span>

<span data-ttu-id="7f51a-112">Essa célula corresponde à opção  Visível na caixa de  diálogo Propriedades  da Camada (na guia Início, no grupo Edição, clique em Camadas e em Propriedades da **Camada).**  </span><span class="sxs-lookup"><span data-stu-id="7f51a-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="7f51a-113">Para obter uma referência para a célula Visible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7f51a-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f51a-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7f51a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7f51a-115">Layers.Visible[ *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7f51a-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7f51a-116">Para obter uma referência para a célula Visible pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7f51a-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f51a-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7f51a-117">Section index:</span></span>  <br/> |<span data-ttu-id="7f51a-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="7f51a-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="7f51a-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="7f51a-119">Row index:</span></span>  <br/> |<span data-ttu-id="7f51a-120">**visRowLayer**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7f51a-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7f51a-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="7f51a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7f51a-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="7f51a-122">**visLayerVisible**</span></span> <br/> |
   

