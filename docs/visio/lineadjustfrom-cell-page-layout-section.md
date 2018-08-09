---
title: Célula LineAdjustFrom (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Determina quais conectores dinâmicos serão separados pelos espaços do aplicativo se forem roteados uns sobre os outros.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772182"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="74d7b-103">Célula LineAdjustFrom (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="74d7b-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="74d7b-104">Determina quais conectores dinâmicos serão separados pelos espaços do aplicativo se forem roteados uns sobre os outros.</span><span class="sxs-lookup"><span data-stu-id="74d7b-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="74d7b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="74d7b-105">**Value**</span></span>|<span data-ttu-id="74d7b-106">**Ajuste**</span><span class="sxs-lookup"><span data-stu-id="74d7b-106">**Adjustment**</span></span>|<span data-ttu-id="74d7b-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="74d7b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74d7b-108">0</span><span class="sxs-lookup"><span data-stu-id="74d7b-108">0</span></span>  <br/> |<span data-ttu-id="74d7b-109">Linhas não relacionadas</span><span class="sxs-lookup"><span data-stu-id="74d7b-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="74d7b-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="74d7b-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="74d7b-111">1</span><span class="sxs-lookup"><span data-stu-id="74d7b-111">1</span></span>  <br/> |<span data-ttu-id="74d7b-112">Todas as linhas</span><span class="sxs-lookup"><span data-stu-id="74d7b-112">All lines</span></span>  <br/> |<span data-ttu-id="74d7b-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="74d7b-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="74d7b-114">2</span><span class="sxs-lookup"><span data-stu-id="74d7b-114">2</span></span>  <br/> |<span data-ttu-id="74d7b-115">Nenhuma linha</span><span class="sxs-lookup"><span data-stu-id="74d7b-115">No lines</span></span>  <br/> |<span data-ttu-id="74d7b-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="74d7b-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="74d7b-117">3</span><span class="sxs-lookup"><span data-stu-id="74d7b-117">3</span></span>  <br/> |<span data-ttu-id="74d7b-118">Padrão de estilo de roteamento</span><span class="sxs-lookup"><span data-stu-id="74d7b-118">Routing style default</span></span>  <br/> |<span data-ttu-id="74d7b-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="74d7b-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74d7b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="74d7b-120">Remarks</span></span>

<span data-ttu-id="74d7b-121">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="74d7b-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="74d7b-122">Para obter uma referência para a célula LineAdjustFrom pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="74d7b-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74d7b-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="74d7b-123">Cell name:</span></span>  <br/> |<span data-ttu-id="74d7b-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="74d7b-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="74d7b-125">Para obter uma referência para a célula LineAdjustFrom pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="74d7b-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74d7b-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="74d7b-126">Section index:</span></span>  <br/> |<span data-ttu-id="74d7b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="74d7b-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="74d7b-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="74d7b-128">Row index:</span></span>  <br/> |<span data-ttu-id="74d7b-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="74d7b-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="74d7b-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="74d7b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="74d7b-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="74d7b-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

