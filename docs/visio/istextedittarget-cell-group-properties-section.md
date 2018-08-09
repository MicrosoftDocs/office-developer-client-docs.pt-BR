---
title: Célula IsTextEditTarget (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Determina a atribuição de texto de um grupo.
ms.openlocfilehash: 65baf90254f6b213efea04739d8e4a66952b2856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772131"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="a6275-103">Célula IsTextEditTarget (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="a6275-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="a6275-104">Determina a atribuição de texto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="a6275-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="a6275-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a6275-105">**Value**</span></span>|<span data-ttu-id="a6275-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a6275-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6275-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="a6275-107">TRUE</span></span>  <br/> |<span data-ttu-id="a6275-108">O texto é adicionado à forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="a6275-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="a6275-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="a6275-109">FALSE</span></span>  <br/> |<span data-ttu-id="a6275-110">O texto é adicionado à forma do grupo no início da ordem de empilhamento.</span><span class="sxs-lookup"><span data-stu-id="a6275-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6275-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6275-111">Remarks</span></span>

<span data-ttu-id="a6275-112">Também é possível definir esse valor selecionando o grupo, clicando em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Editar texto do grupo**.</span><span class="sxs-lookup"><span data-stu-id="a6275-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="a6275-p101">Os grupos criados em versões anteriores ao Visio 2000 têm um valor padrão de FALSO. A partir do Visio versão 2000, o valor padrão é VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="a6275-p101">Groups created in versions earlier than Visio 2000 have a default value of FALSE. Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="a6275-115">Para obter uma referência para a célula IsTextEditTarget pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a6275-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6275-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a6275-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a6275-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="a6275-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="a6275-118">Para obter uma referência para a célula IsTextEditTarget pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a6275-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6275-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a6275-119">Section index:</span></span>  <br/> |<span data-ttu-id="a6275-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6275-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a6275-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a6275-121">Row index:</span></span>  <br/> |<span data-ttu-id="a6275-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="a6275-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="a6275-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a6275-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a6275-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="a6275-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

