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
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421617"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="3a723-103">Célula ConLineJumpCode (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="3a723-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3a723-104">Determina quando um conector salta.</span><span class="sxs-lookup"><span data-stu-id="3a723-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="3a723-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3a723-105">**Value**</span></span>|<span data-ttu-id="3a723-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a723-106">**Description**</span></span>|<span data-ttu-id="3a723-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="3a723-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3a723-108">,0</span><span class="sxs-lookup"><span data-stu-id="3a723-108">0</span></span>  <br/> |<span data-ttu-id="3a723-109">Como especificado na página, no menu **Design**, clique na seta do grupo **Configurar Página** e na guia **Layout e Direcionamento** para ver as especificações da página.</span><span class="sxs-lookup"><span data-stu-id="3a723-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="3a723-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="3a723-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="3a723-111">1</span><span class="sxs-lookup"><span data-stu-id="3a723-111">1</span></span>  <br/> |<span data-ttu-id="3a723-112">Nunca</span><span class="sxs-lookup"><span data-stu-id="3a723-112">Never</span></span>  <br/> |<span data-ttu-id="3a723-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="3a723-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="3a723-114">duas</span><span class="sxs-lookup"><span data-stu-id="3a723-114">2</span></span>  <br/> |<span data-ttu-id="3a723-115">Sempre</span><span class="sxs-lookup"><span data-stu-id="3a723-115">Always</span></span>  <br/> |<span data-ttu-id="3a723-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="3a723-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="3a723-117">3D</span><span class="sxs-lookup"><span data-stu-id="3a723-117">3</span></span>  <br/> |<span data-ttu-id="3a723-118">Outro conector salta</span><span class="sxs-lookup"><span data-stu-id="3a723-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="3a723-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="3a723-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="3a723-120">4 </span><span class="sxs-lookup"><span data-stu-id="3a723-120">4</span></span>  <br/> |<span data-ttu-id="3a723-121">Nenhum conector salta</span><span class="sxs-lookup"><span data-stu-id="3a723-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="3a723-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="3a723-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a723-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a723-123">Remarks</span></span>

<span data-ttu-id="3a723-124">Também é possível definir o valor desta célula selecionando um conector dinâmico, clicando em **Comportamento**, no grupo **Design da Forma**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **Conector**.</span><span class="sxs-lookup"><span data-stu-id="3a723-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="3a723-125">Para obter uma referência para a célula ConLineJumpCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3a723-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a723-126">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3a723-126">Cell name:</span></span>  <br/> |<span data-ttu-id="3a723-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="3a723-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="3a723-128">Para obter uma referência para a célula ConLineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3a723-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a723-129">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3a723-129">Section index:</span></span>  <br/> |<span data-ttu-id="3a723-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a723-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3a723-131">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3a723-131">Row index:</span></span>  <br/> |<span data-ttu-id="3a723-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3a723-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="3a723-133">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3a723-133">Cell index:</span></span>  <br/> |<span data-ttu-id="3a723-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="3a723-134">**visSLOJumpCode**</span></span> <br/> |
   

