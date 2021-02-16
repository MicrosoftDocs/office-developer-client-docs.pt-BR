---
title: Célula IsDropSource (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Determina se a forma pode ser adicionada ao grupo sendo solta nele.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421890"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="9ec41-103">Célula IsDropSource (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="9ec41-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="9ec41-104">Determina se a forma pode ser adicionada ao grupo sendo solta nele.</span><span class="sxs-lookup"><span data-stu-id="9ec41-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="9ec41-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9ec41-105">**Value**</span></span>|<span data-ttu-id="9ec41-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9ec41-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ec41-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="9ec41-107">TRUE</span></span>  <br/> |<span data-ttu-id="9ec41-108">A forma pode ser adicionada ao grupo sendo solta nele.</span><span class="sxs-lookup"><span data-stu-id="9ec41-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="9ec41-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9ec41-109">FALSE</span></span>  <br/> |<span data-ttu-id="9ec41-110">A forma não pode ser adicionada ao grupo.</span><span class="sxs-lookup"><span data-stu-id="9ec41-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ec41-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ec41-111">Remarks</span></span>

<span data-ttu-id="9ec41-112">Também é possível definir esse valor selecionando a forma, clicando em **Comportamento** na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Adicionar forma aos grupos ao soltar**.</span><span class="sxs-lookup"><span data-stu-id="9ec41-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="9ec41-p101">Além de ativar esse comportamento para uma forma, também é necessário ativar um grupo que aceite formas arrastadas para dentro dele. Para fazer isso, clique em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, marque a caixa de seleção **Aceitar formas soltas**. Este valor será armazenado na célula IsDropTarget na seção Group Properties.</span><span class="sxs-lookup"><span data-stu-id="9ec41-p101">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it. To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box. This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="9ec41-116">Para obter uma referência para a célula IsDropSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9ec41-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ec41-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9ec41-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9ec41-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="9ec41-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="9ec41-119">Para obter uma referência para a célula IsDropSource pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9ec41-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ec41-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9ec41-120">Section index:</span></span>  <br/> |<span data-ttu-id="9ec41-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ec41-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9ec41-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="9ec41-122">Row index:</span></span>  <br/> |<span data-ttu-id="9ec41-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="9ec41-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="9ec41-124">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="9ec41-124">Cell index:</span></span>  <br/> |<span data-ttu-id="9ec41-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="9ec41-125">**visDropSource**</span></span> <br/> |
   

