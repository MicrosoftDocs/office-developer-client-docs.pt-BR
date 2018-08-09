---
title: Célula ShapePlowCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Determina se esta forma de colocação será movida ao soltar outra forma de colocação próxima a esta forma na página de desenho.
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772907"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="852ba-103">Célula ShapePlowCode (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="852ba-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="852ba-104">Determina se esta forma de colocação será movida ao soltar outra forma de colocação próxima a esta forma na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="852ba-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="852ba-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="852ba-105">**Value**</span></span>|<span data-ttu-id="852ba-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="852ba-106">**Description**</span></span>|<span data-ttu-id="852ba-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="852ba-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="852ba-108">0</span><span class="sxs-lookup"><span data-stu-id="852ba-108">0</span></span>  <br/> |<span data-ttu-id="852ba-109">Ajustar como especificado na página.</span><span class="sxs-lookup"><span data-stu-id="852ba-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="852ba-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="852ba-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="852ba-111">1</span><span class="sxs-lookup"><span data-stu-id="852ba-111">1</span></span>  <br/> |<span data-ttu-id="852ba-112">Não ajustar formas.</span><span class="sxs-lookup"><span data-stu-id="852ba-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="852ba-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="852ba-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="852ba-114">2</span><span class="sxs-lookup"><span data-stu-id="852ba-114">2</span></span>  <br/> |<span data-ttu-id="852ba-115">Ajustar todas as formas.</span><span class="sxs-lookup"><span data-stu-id="852ba-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="852ba-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="852ba-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="852ba-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="852ba-117">Remarks</span></span>

<span data-ttu-id="852ba-118">Você também pode definir o valor dessa célula para uma determinada forma na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e clique no Guia de **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="852ba-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="852ba-119">Para definir esse comportamento para *todas* as formas na página de desenho, use a célula PlowCode na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="852ba-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="852ba-120">Para obter uma referência para a célula ShapePlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="852ba-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="852ba-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="852ba-121">Cell name:</span></span>  <br/> |<span data-ttu-id="852ba-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="852ba-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="852ba-123">Para obter uma referência para a célula ShapePlowCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="852ba-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="852ba-124">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="852ba-124">Section index:</span></span>  <br/> |<span data-ttu-id="852ba-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="852ba-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="852ba-126">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="852ba-126">Row index:</span></span>  <br/> |<span data-ttu-id="852ba-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="852ba-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="852ba-128">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="852ba-128">Cell index:</span></span>  <br/> |<span data-ttu-id="852ba-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="852ba-129">**visSLOPlowCode**</span></span> <br/> |
   

