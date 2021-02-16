---
title: Célula LineJumpCode (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Determina os conectores aos quais você deseja adicionar saltos.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416248"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="68954-103">Célula LineJumpCode (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="68954-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="68954-104">Determina os conectores aos quais você deseja adicionar saltos.</span><span class="sxs-lookup"><span data-stu-id="68954-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="68954-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="68954-105">**Value**</span></span>|<span data-ttu-id="68954-106">**Conectores aos quais você deseja adicionar saltos**</span><span class="sxs-lookup"><span data-stu-id="68954-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="68954-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="68954-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68954-108">0</span><span class="sxs-lookup"><span data-stu-id="68954-108">0</span></span>  <br/> |<span data-ttu-id="68954-109">Nenhum</span><span class="sxs-lookup"><span data-stu-id="68954-109">None</span></span>  <br/> |<span data-ttu-id="68954-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="68954-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="68954-111">1 </span><span class="sxs-lookup"><span data-stu-id="68954-111">1</span></span>  <br/> |<span data-ttu-id="68954-112">Linhas horizontais</span><span class="sxs-lookup"><span data-stu-id="68954-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="68954-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="68954-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="68954-114">2 </span><span class="sxs-lookup"><span data-stu-id="68954-114">2</span></span>  <br/> |<span data-ttu-id="68954-115">Linhas verticais</span><span class="sxs-lookup"><span data-stu-id="68954-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="68954-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="68954-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="68954-117">3 </span><span class="sxs-lookup"><span data-stu-id="68954-117">3</span></span>  <br/> |<span data-ttu-id="68954-118">Última linha circulada</span><span class="sxs-lookup"><span data-stu-id="68954-118">Last routed line</span></span>  <br/> |<span data-ttu-id="68954-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="68954-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="68954-120">4 </span><span class="sxs-lookup"><span data-stu-id="68954-120">4</span></span>  <br/> |<span data-ttu-id="68954-121">Última linha exibida (forma superior na ordem *z)*</span><span class="sxs-lookup"><span data-stu-id="68954-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="68954-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="68954-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="68954-123">5 </span><span class="sxs-lookup"><span data-stu-id="68954-123">5</span></span>  <br/> |<span data-ttu-id="68954-124">Primeira linha exibida (forma na parte inferior da ordem *z)*</span><span class="sxs-lookup"><span data-stu-id="68954-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="68954-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="68954-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68954-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="68954-126">Remarks</span></span>

<span data-ttu-id="68954-127">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="68954-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="68954-128">Para obter uma referência para a célula LineJumpCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="68954-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68954-129">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="68954-129">Cell name:</span></span>  <br/> |<span data-ttu-id="68954-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="68954-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="68954-131">Para obter uma referência para a célula LineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="68954-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68954-132">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="68954-132">Section index:</span></span>  <br/> |<span data-ttu-id="68954-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68954-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="68954-134">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="68954-134">Row index:</span></span>  <br/> |<span data-ttu-id="68954-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="68954-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="68954-136">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="68954-136">Cell index:</span></span>  <br/> |<span data-ttu-id="68954-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="68954-137">**visPLOJumpCode**</span></span> <br/> |
   

