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
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423892"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="761cf-103">Célula ShapePlowCode (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="761cf-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="761cf-104">Determina se esta forma de colocação será movida ao soltar outra forma de colocação próxima a esta forma na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="761cf-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="761cf-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="761cf-105">**Value**</span></span>|<span data-ttu-id="761cf-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="761cf-106">**Description**</span></span>|<span data-ttu-id="761cf-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="761cf-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="761cf-108">,0</span><span class="sxs-lookup"><span data-stu-id="761cf-108">0</span></span>  <br/> |<span data-ttu-id="761cf-109">Ajustar como especificado na página.</span><span class="sxs-lookup"><span data-stu-id="761cf-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="761cf-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="761cf-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="761cf-111">1</span><span class="sxs-lookup"><span data-stu-id="761cf-111">1</span></span>  <br/> |<span data-ttu-id="761cf-112">Não ajustar formas.</span><span class="sxs-lookup"><span data-stu-id="761cf-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="761cf-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="761cf-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="761cf-114">duas</span><span class="sxs-lookup"><span data-stu-id="761cf-114">2</span></span>  <br/> |<span data-ttu-id="761cf-115">Ajustar todas as formas.</span><span class="sxs-lookup"><span data-stu-id="761cf-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="761cf-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="761cf-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="761cf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="761cf-117">Remarks</span></span>

<span data-ttu-id="761cf-118">Você também pode definir o valor dessa célula para uma forma específica na guia **posicionamento** da caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique no botão Guia **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="761cf-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="761cf-119">Para definir esse comportamento para *todas* as formas na página de desenho, use a célula PlowCode na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="761cf-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="761cf-120">Para obter uma referência para a célula ShapePlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="761cf-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="761cf-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="761cf-121">Cell name:</span></span>  <br/> |<span data-ttu-id="761cf-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="761cf-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="761cf-123">Para obter uma referência para a célula ShapePlowCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="761cf-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="761cf-124">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="761cf-124">Section index:</span></span>  <br/> |<span data-ttu-id="761cf-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="761cf-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="761cf-126">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="761cf-126">Row index:</span></span>  <br/> |<span data-ttu-id="761cf-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="761cf-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="761cf-128">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="761cf-128">Cell index:</span></span>  <br/> |<span data-ttu-id="761cf-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="761cf-129">**visSLOPlowCode**</span></span> <br/> |
   

