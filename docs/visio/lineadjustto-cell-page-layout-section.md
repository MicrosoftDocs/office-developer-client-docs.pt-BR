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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414022"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="b346c-103">Célula LineAdjustTo (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="b346c-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="b346c-104">Determina quais conectores dinâmicos são alinhados uns sobre os outros.</span><span class="sxs-lookup"><span data-stu-id="b346c-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="b346c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b346c-105">**Value**</span></span>|<span data-ttu-id="b346c-106">**Ajuste**</span><span class="sxs-lookup"><span data-stu-id="b346c-106">**Adjustment**</span></span>|<span data-ttu-id="b346c-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="b346c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b346c-108">0</span><span class="sxs-lookup"><span data-stu-id="b346c-108">0</span></span>  <br/> |<span data-ttu-id="b346c-109">Padrão de estilo de roteamento</span><span class="sxs-lookup"><span data-stu-id="b346c-109">Routing style default</span></span>  <br/> |<span data-ttu-id="b346c-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="b346c-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="b346c-111">1 </span><span class="sxs-lookup"><span data-stu-id="b346c-111">1</span></span>  <br/> |<span data-ttu-id="b346c-112">Linhas próximas umas das outras</span><span class="sxs-lookup"><span data-stu-id="b346c-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="b346c-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="b346c-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="b346c-114">2 </span><span class="sxs-lookup"><span data-stu-id="b346c-114">2</span></span>  <br/> |<span data-ttu-id="b346c-115">Nenhuma linha</span><span class="sxs-lookup"><span data-stu-id="b346c-115">No lines</span></span>  <br/> |<span data-ttu-id="b346c-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="b346c-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="b346c-117">3 </span><span class="sxs-lookup"><span data-stu-id="b346c-117">3</span></span>  <br/> |<span data-ttu-id="b346c-118">Linhas relacionadas</span><span class="sxs-lookup"><span data-stu-id="b346c-118">Related lines</span></span>  <br/> |<span data-ttu-id="b346c-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="b346c-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b346c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b346c-120">Remarks</span></span>

<span data-ttu-id="b346c-121">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="b346c-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="b346c-122">Para obter uma referência para a célula LineAdjustTo pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b346c-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b346c-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b346c-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b346c-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="b346c-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="b346c-125">Para obter uma referência para a célula LineAdjustTo pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b346c-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b346c-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b346c-126">Section index:</span></span>  <br/> |<span data-ttu-id="b346c-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b346c-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b346c-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b346c-128">Row index:</span></span>  <br/> |<span data-ttu-id="b346c-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b346c-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b346c-130">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="b346c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b346c-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="b346c-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

