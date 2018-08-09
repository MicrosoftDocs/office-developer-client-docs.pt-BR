---
title: Célula ConLineJumpCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Determina quando um conector salta.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771581"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="69c01-103">Célula ConLineJumpCode (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="69c01-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="69c01-104">Determina quando um conector salta.</span><span class="sxs-lookup"><span data-stu-id="69c01-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="69c01-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69c01-105">**Value**</span></span>|<span data-ttu-id="69c01-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="69c01-106">**Description**</span></span>|<span data-ttu-id="69c01-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="69c01-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69c01-108">0</span><span class="sxs-lookup"><span data-stu-id="69c01-108">0</span></span>  <br/> |<span data-ttu-id="69c01-109">
          Como especificado na página, no menu **Design**, clique na seta do grupo **Configurar Página** e na guia **Layout e Direcionamento** para ver as especificações da página.
</span><span class="sxs-lookup"><span data-stu-id="69c01-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="69c01-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="69c01-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="69c01-111">1</span><span class="sxs-lookup"><span data-stu-id="69c01-111">1</span></span>  <br/> |<span data-ttu-id="69c01-112">Nunca</span><span class="sxs-lookup"><span data-stu-id="69c01-112">Never</span></span>  <br/> |<span data-ttu-id="69c01-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="69c01-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="69c01-114">2</span><span class="sxs-lookup"><span data-stu-id="69c01-114">2</span></span>  <br/> |<span data-ttu-id="69c01-115">Sempre</span><span class="sxs-lookup"><span data-stu-id="69c01-115">Always</span></span>  <br/> |<span data-ttu-id="69c01-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="69c01-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="69c01-117">3</span><span class="sxs-lookup"><span data-stu-id="69c01-117">3</span></span>  <br/> |<span data-ttu-id="69c01-118">Outro conector salta</span><span class="sxs-lookup"><span data-stu-id="69c01-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="69c01-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="69c01-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="69c01-120">4</span><span class="sxs-lookup"><span data-stu-id="69c01-120">4</span></span>  <br/> |<span data-ttu-id="69c01-121">
          Nenhum conector salta
</span><span class="sxs-lookup"><span data-stu-id="69c01-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="69c01-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="69c01-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69c01-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="69c01-123">Remarks</span></span>

<span data-ttu-id="69c01-124">Você pode também definir o valor desta célula selecionando um conector dinâmico, clicando em **comportamento** , no grupo **Design** da forma na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **conector** .</span><span class="sxs-lookup"><span data-stu-id="69c01-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="69c01-125">Para obter uma referência para a célula ConLineJumpCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="69c01-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69c01-126">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="69c01-126">Cell name:</span></span>  <br/> |<span data-ttu-id="69c01-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="69c01-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="69c01-128">Para obter uma referência para a célula ConLineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="69c01-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69c01-129">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="69c01-129">Section index:</span></span>  <br/> |<span data-ttu-id="69c01-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="69c01-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="69c01-131">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="69c01-131">Row index:</span></span>  <br/> |<span data-ttu-id="69c01-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="69c01-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="69c01-133">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="69c01-133">Cell index:</span></span>  <br/> |<span data-ttu-id="69c01-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="69c01-134">**visSLOJumpCode**</span></span> <br/> |
   

