---
title: Célula ResizeMode (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Mostra a definição de comportamento de redimensionamento atual da forma.
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772753"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="b023e-103">Célula ResizeMode (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="b023e-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="b023e-104">Mostra a definição de comportamento de redimensionamento atual da forma.</span><span class="sxs-lookup"><span data-stu-id="b023e-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="b023e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b023e-105">**Value**</span></span>|<span data-ttu-id="b023e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b023e-106">**Description**</span></span>|<span data-ttu-id="b023e-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="b023e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b023e-108">0</span><span class="sxs-lookup"><span data-stu-id="b023e-108">0</span></span>  <br/> |<span data-ttu-id="b023e-109">Usar configuração do grupo.</span><span class="sxs-lookup"><span data-stu-id="b023e-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="b023e-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="b023e-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="b023e-111">1</span><span class="sxs-lookup"><span data-stu-id="b023e-111">1</span></span>  <br/> |<span data-ttu-id="b023e-112">Apenas reposicionar.</span><span class="sxs-lookup"><span data-stu-id="b023e-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="b023e-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="b023e-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="b023e-114">2</span><span class="sxs-lookup"><span data-stu-id="b023e-114">2</span></span>  <br/> |<span data-ttu-id="b023e-115">Escala com grupo.</span><span class="sxs-lookup"><span data-stu-id="b023e-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="b023e-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="b023e-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b023e-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b023e-117">Remarks</span></span>

<span data-ttu-id="b023e-118">Você também pode definir esse valor na guia **comportamento** , na caixa de diálogo **comportamento** (na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md), no grupo **Design da forma** , clique em **comportamento**).</span><span class="sxs-lookup"><span data-stu-id="b023e-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="b023e-119">Para obter uma referência à célula ResizeMode pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b023e-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b023e-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b023e-120">Cell name:</span></span>  <br/> |<span data-ttu-id="b023e-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="b023e-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="b023e-122">Para obter uma referência à célula ResizeMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b023e-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b023e-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b023e-123">Section index:</span></span>  <br/> |<span data-ttu-id="b023e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b023e-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b023e-125">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b023e-125">Row index:</span></span>  <br/> |<span data-ttu-id="b023e-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="b023e-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="b023e-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b023e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="b023e-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="b023e-128">**visXFormResizeMode**</span></span> <br/> |
   

