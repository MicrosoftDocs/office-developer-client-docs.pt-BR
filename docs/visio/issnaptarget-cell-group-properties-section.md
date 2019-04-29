---
title: Célula IsSnapTarget (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Determina o ajuste a um grupo ou a formas no grupo.
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421442"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="020d2-103">Célula IsSnapTarget (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="020d2-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="020d2-104">Determina o ajuste a um grupo ou a formas no grupo.</span><span class="sxs-lookup"><span data-stu-id="020d2-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="020d2-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="020d2-105">**Value**</span></span>|<span data-ttu-id="020d2-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="020d2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="020d2-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="020d2-107">TRUE</span></span>  <br/> |<span data-ttu-id="020d2-108">Permite ajustar a formas no grupo.</span><span class="sxs-lookup"><span data-stu-id="020d2-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="020d2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="020d2-109">FALSE</span></span>  <br/> |<span data-ttu-id="020d2-110">Permite ajustar somente ao grupo.</span><span class="sxs-lookup"><span data-stu-id="020d2-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="020d2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="020d2-111">Remarks</span></span>

<span data-ttu-id="020d2-112">Também é possível definir esse valor selecionando o grupo, clicando em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Ajustar às formas do membro**.</span><span class="sxs-lookup"><span data-stu-id="020d2-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="020d2-113">Para obter uma referência para a célula IsSnapTarget pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="020d2-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="020d2-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="020d2-114">Cell name:</span></span>  <br/> |<span data-ttu-id="020d2-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="020d2-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="020d2-116">Para obter uma referência para a célula IsSnapTarget pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="020d2-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="020d2-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="020d2-117">Section index:</span></span>  <br/> |<span data-ttu-id="020d2-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="020d2-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="020d2-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="020d2-119">Row index:</span></span>  <br/> |<span data-ttu-id="020d2-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="020d2-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="020d2-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="020d2-121">Cell index:</span></span>  <br/> |<span data-ttu-id="020d2-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="020d2-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

