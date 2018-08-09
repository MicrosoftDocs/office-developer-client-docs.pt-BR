---
title: Célula LineAdjustTo (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Determina quais conectores dinâmicos são alinhados uns sobre os outros.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772193"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="7b88b-103">Célula LineAdjustTo (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="7b88b-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="7b88b-104">Determina quais conectores dinâmicos são alinhados uns sobre os outros.</span><span class="sxs-lookup"><span data-stu-id="7b88b-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="7b88b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7b88b-105">**Value**</span></span>|<span data-ttu-id="7b88b-106">**Ajuste**</span><span class="sxs-lookup"><span data-stu-id="7b88b-106">**Adjustment**</span></span>|<span data-ttu-id="7b88b-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="7b88b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b88b-108">0</span><span class="sxs-lookup"><span data-stu-id="7b88b-108">0</span></span>  <br/> |<span data-ttu-id="7b88b-109">Padrão de estilo de roteamento</span><span class="sxs-lookup"><span data-stu-id="7b88b-109">Routing style default</span></span>  <br/> |<span data-ttu-id="7b88b-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="7b88b-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="7b88b-111">1</span><span class="sxs-lookup"><span data-stu-id="7b88b-111">1</span></span>  <br/> |<span data-ttu-id="7b88b-112">Linhas próximas umas das outras</span><span class="sxs-lookup"><span data-stu-id="7b88b-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="7b88b-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="7b88b-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="7b88b-114">2</span><span class="sxs-lookup"><span data-stu-id="7b88b-114">2</span></span>  <br/> |<span data-ttu-id="7b88b-115">Nenhuma linha</span><span class="sxs-lookup"><span data-stu-id="7b88b-115">No lines</span></span>  <br/> |<span data-ttu-id="7b88b-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="7b88b-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="7b88b-117">3</span><span class="sxs-lookup"><span data-stu-id="7b88b-117">3</span></span>  <br/> |<span data-ttu-id="7b88b-118">Linhas relacionadas</span><span class="sxs-lookup"><span data-stu-id="7b88b-118">Related lines</span></span>  <br/> |<span data-ttu-id="7b88b-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="7b88b-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b88b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b88b-120">Remarks</span></span>

<span data-ttu-id="7b88b-121">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="7b88b-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="7b88b-122">Para obter uma referência para a célula LineAdjustTo pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7b88b-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b88b-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7b88b-123">Cell name:</span></span>  <br/> |<span data-ttu-id="7b88b-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="7b88b-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="7b88b-125">Para obter uma referência para a célula LineAdjustTo pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7b88b-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b88b-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7b88b-126">Section index:</span></span>  <br/> |<span data-ttu-id="7b88b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b88b-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7b88b-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7b88b-128">Row index:</span></span>  <br/> |<span data-ttu-id="7b88b-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="7b88b-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="7b88b-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7b88b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7b88b-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="7b88b-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

