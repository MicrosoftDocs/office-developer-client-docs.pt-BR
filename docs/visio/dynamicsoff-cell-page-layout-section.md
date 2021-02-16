---
title: Célula DynamicsOff (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Determina se as formas de colocação serão movidas e se os conectores serão redirecionados em torno de outras formas e outros conectores na página de desenho.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437473"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="ee909-103">Célula DynamicsOff (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="ee909-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="ee909-104">Determina se as formas de colocação serão movidas e se os conectores serão redirecionados em torno de outras formas e outros conectores na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="ee909-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="ee909-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ee909-105">**Value**</span></span>|<span data-ttu-id="ee909-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ee909-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ee909-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="ee909-107">TRUE</span></span>  <br/> | <span data-ttu-id="ee909-108">Desativar dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ee909-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="ee909-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ee909-109">FALSE</span></span>  <br/> | <span data-ttu-id="ee909-110">Ativar dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ee909-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee909-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee909-111">Remarks</span></span>

<span data-ttu-id="ee909-p101">É possível desativar a dinâmica para aumentar o desempenho de sua solução. Por exemplo, se a sua solução adiciona formas de colocação a um desenho e você não quer que o aplicativo redirecione os conectores e reposicione as formas sempre que uma forma for adicionada, desative a dinâmica. Depois que a solução adicionar as formas, ative a dinâmica novamente.</span><span class="sxs-lookup"><span data-stu-id="ee909-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="ee909-115">Para fazer referência à célula DynamicsOff pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ee909-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee909-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ee909-116">Cell name:</span></span>  <br/> | <span data-ttu-id="ee909-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="ee909-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="ee909-118">Para fazer referência à célula DynamicsOff pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ee909-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee909-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ee909-119">Section index:</span></span>  <br/> |<span data-ttu-id="ee909-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee909-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ee909-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ee909-121">Row index:</span></span>  <br/> |<span data-ttu-id="ee909-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="ee909-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="ee909-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ee909-123">Cell index:</span></span>  <br/> |<span data-ttu-id="ee909-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="ee909-124">**visPLODynamicsOff**</span></span> <br/> |
   

