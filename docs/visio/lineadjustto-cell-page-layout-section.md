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
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359308"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="470c3-103">Célula LineAdjustTo (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="470c3-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="470c3-104">Determina quais conectores dinâmicos são alinhados uns sobre os outros.</span><span class="sxs-lookup"><span data-stu-id="470c3-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="470c3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="470c3-105">**Value**</span></span>|<span data-ttu-id="470c3-106">**Just**</span><span class="sxs-lookup"><span data-stu-id="470c3-106">**Adjustment**</span></span>|<span data-ttu-id="470c3-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="470c3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="470c3-108">,0</span><span class="sxs-lookup"><span data-stu-id="470c3-108">0</span></span>  <br/> |<span data-ttu-id="470c3-109">Padrão de estilo de roteamento</span><span class="sxs-lookup"><span data-stu-id="470c3-109">Routing style default</span></span>  <br/> |<span data-ttu-id="470c3-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="470c3-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="470c3-111">1</span><span class="sxs-lookup"><span data-stu-id="470c3-111">1</span></span>  <br/> |<span data-ttu-id="470c3-112">Linhas próximas umas das outras</span><span class="sxs-lookup"><span data-stu-id="470c3-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="470c3-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="470c3-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="470c3-114">duas</span><span class="sxs-lookup"><span data-stu-id="470c3-114">2</span></span>  <br/> |<span data-ttu-id="470c3-115">Nenhuma linha</span><span class="sxs-lookup"><span data-stu-id="470c3-115">No lines</span></span>  <br/> |<span data-ttu-id="470c3-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="470c3-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="470c3-117">3D</span><span class="sxs-lookup"><span data-stu-id="470c3-117">3</span></span>  <br/> |<span data-ttu-id="470c3-118">Linhas relacionadas</span><span class="sxs-lookup"><span data-stu-id="470c3-118">Related lines</span></span>  <br/> |<span data-ttu-id="470c3-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="470c3-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="470c3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="470c3-120">Remarks</span></span>

<span data-ttu-id="470c3-121">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="470c3-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="470c3-122">Para obter uma referência para a célula LineAdjustTo pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="470c3-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="470c3-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="470c3-123">Cell name:</span></span>  <br/> |<span data-ttu-id="470c3-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="470c3-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="470c3-125">Para obter uma referência para a célula LineAdjustTo pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="470c3-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="470c3-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="470c3-126">Section index:</span></span>  <br/> |<span data-ttu-id="470c3-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="470c3-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="470c3-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="470c3-128">Row index:</span></span>  <br/> |<span data-ttu-id="470c3-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="470c3-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="470c3-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="470c3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="470c3-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="470c3-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

