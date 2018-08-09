---
title: Célula IsDropTarget (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Determina se a forma pode ser adicionada ao grupo sendo solta nele.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772103"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="916b5-103">Célula IsDropTarget (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="916b5-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="916b5-104">Determina se a forma pode ser adicionada ao grupo sendo solta nele.</span><span class="sxs-lookup"><span data-stu-id="916b5-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="916b5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="916b5-105">**Value**</span></span>|<span data-ttu-id="916b5-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="916b5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="916b5-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="916b5-107">TRUE</span></span>  <br/> |<span data-ttu-id="916b5-108">A forma pode ser adicionada ao grupo sendo solta nele.</span><span class="sxs-lookup"><span data-stu-id="916b5-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="916b5-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="916b5-109">FALSE</span></span>  <br/> |<span data-ttu-id="916b5-110">A forma não pode ser solta no grupo.</span><span class="sxs-lookup"><span data-stu-id="916b5-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="916b5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="916b5-111">Remarks</span></span>

<span data-ttu-id="916b5-112">Também é possível definir esse valor selecionando o grupo, clicando em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Aceitar formas soltas**.</span><span class="sxs-lookup"><span data-stu-id="916b5-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="916b5-p101">Para adicionar uma forma soltando-a no grupo, você também deve ativar um comportamento de forma semelhante. Selecione a forma, clique em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, marque a caixa de seleção **Adicionar forma aos grupos ao soltar**. Esse valor será armazenado na célula IsDropSource na seção Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="916b5-p101">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior. You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box. This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="916b5-116">Para obter uma referência para a célula IsDropTarget pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="916b5-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="916b5-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="916b5-117">Cell name:</span></span>  <br/> |<span data-ttu-id="916b5-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="916b5-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="916b5-119">Para obter uma referência para a célula IsDropTarget pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="916b5-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="916b5-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="916b5-120">Section index:</span></span>  <br/> |<span data-ttu-id="916b5-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="916b5-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="916b5-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="916b5-122">Row index:</span></span>  <br/> |<span data-ttu-id="916b5-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="916b5-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="916b5-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="916b5-124">Cell index:</span></span>  <br/> |<span data-ttu-id="916b5-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="916b5-125">**visGroupIsDropTarget**</span></span> <br/> |
   

