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
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772190"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="5a59d-103">Célula LineJumpCode (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="5a59d-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="5a59d-104">Determina os conectores aos quais você deseja adicionar saltos.</span><span class="sxs-lookup"><span data-stu-id="5a59d-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="5a59d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5a59d-105">**Value**</span></span>|<span data-ttu-id="5a59d-106">**Conectores aos quais você deseja adicionar saltos**</span><span class="sxs-lookup"><span data-stu-id="5a59d-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="5a59d-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="5a59d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a59d-108">0</span><span class="sxs-lookup"><span data-stu-id="5a59d-108">0</span></span>  <br/> |<span data-ttu-id="5a59d-109">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5a59d-109">None</span></span>  <br/> |<span data-ttu-id="5a59d-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="5a59d-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="5a59d-111">1</span><span class="sxs-lookup"><span data-stu-id="5a59d-111">1</span></span>  <br/> |<span data-ttu-id="5a59d-112">Linhas horizontais</span><span class="sxs-lookup"><span data-stu-id="5a59d-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="5a59d-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="5a59d-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="5a59d-114">2</span><span class="sxs-lookup"><span data-stu-id="5a59d-114">2</span></span>  <br/> |<span data-ttu-id="5a59d-115">Linhas verticais</span><span class="sxs-lookup"><span data-stu-id="5a59d-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="5a59d-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="5a59d-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="5a59d-117">3</span><span class="sxs-lookup"><span data-stu-id="5a59d-117">3</span></span>  <br/> |<span data-ttu-id="5a59d-118">Última linha circulada</span><span class="sxs-lookup"><span data-stu-id="5a59d-118">Last routed line</span></span>  <br/> |<span data-ttu-id="5a59d-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="5a59d-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="5a59d-120">4</span><span class="sxs-lookup"><span data-stu-id="5a59d-120">4</span></span>  <br/> |<span data-ttu-id="5a59d-121">Última linha exibida (primeira forma na *z* -ordem)</span><span class="sxs-lookup"><span data-stu-id="5a59d-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="5a59d-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="5a59d-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="5a59d-123">5</span><span class="sxs-lookup"><span data-stu-id="5a59d-123">5</span></span>  <br/> |<span data-ttu-id="5a59d-124">Primeira linha exibida (forma no fim de a *z* -ordem)</span><span class="sxs-lookup"><span data-stu-id="5a59d-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="5a59d-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="5a59d-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a59d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a59d-126">Remarks</span></span>

<span data-ttu-id="5a59d-127">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="5a59d-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="5a59d-128">Para obter uma referência para a célula LineJumpCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="5a59d-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a59d-129">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5a59d-129">Cell name:</span></span>  <br/> |<span data-ttu-id="5a59d-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="5a59d-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="5a59d-131">Para obter uma referência para a célula LineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5a59d-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a59d-132">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5a59d-132">Section index:</span></span>  <br/> |<span data-ttu-id="5a59d-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5a59d-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5a59d-134">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5a59d-134">Row index:</span></span>  <br/> |<span data-ttu-id="5a59d-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="5a59d-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="5a59d-136">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5a59d-136">Cell index:</span></span>  <br/> |<span data-ttu-id="5a59d-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="5a59d-137">**visPLOJumpCode**</span></span> <br/> |
   

