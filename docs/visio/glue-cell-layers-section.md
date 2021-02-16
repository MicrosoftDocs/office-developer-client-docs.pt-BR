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
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408513"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="3d855-103">Célula Glue (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="3d855-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="3d855-104">Especifica se as formas pertencentes à camada podem ser coladas.</span><span class="sxs-lookup"><span data-stu-id="3d855-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="3d855-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3d855-105">**Value**</span></span>|<span data-ttu-id="3d855-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3d855-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d855-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="3d855-107">TRUE</span></span>  <br/> |<span data-ttu-id="3d855-108">A cola está ativada.</span><span class="sxs-lookup"><span data-stu-id="3d855-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="3d855-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3d855-109">FALSE</span></span>  <br/> |<span data-ttu-id="3d855-110">A cola não está ativada.</span><span class="sxs-lookup"><span data-stu-id="3d855-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d855-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d855-111">Remarks</span></span>

<span data-ttu-id="3d855-112">Essa célula corresponde à opção  Colar na caixa de  diálogo Propriedades  da Camada (na guia Início, no grupo Edição, clique em Camadas e em Propriedades da **Camada).**  </span><span class="sxs-lookup"><span data-stu-id="3d855-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="3d855-113">Para obter uma referência para a célula Glue pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3d855-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d855-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3d855-114">Cell name:</span></span>  <br/> |<span data-ttu-id="3d855-115">Layers.Glue[  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3d855-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3d855-116">Para obter uma referência para a célula Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3d855-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d855-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3d855-117">Section index:</span></span>  <br/> |<span data-ttu-id="3d855-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="3d855-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="3d855-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3d855-119">Row index:</span></span>  <br/> |<span data-ttu-id="3d855-120">**visRowLayer**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3d855-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3d855-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3d855-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3d855-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="3d855-122">**visLayerGlue**</span></span> <br/> |
   

