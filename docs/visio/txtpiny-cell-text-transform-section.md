---
title: Célula TxtPinY (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Determina a coordenada y do centro de rotação do bloco de texto em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316419"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="e5d3a-104">Célula TxtPinY (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="e5d3a-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="e5d3a-105">Determina a coordenada *y* do centro de rotação do bloco de texto em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="e5d3a-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="e5d3a-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-106">The default formula is:</span></span> 
  
<span data-ttu-id="e5d3a-107">= Altura \* 0,5</span><span class="sxs-lookup"><span data-stu-id="e5d3a-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5d3a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5d3a-108">Remarks</span></span>

<span data-ttu-id="e5d3a-109">Para fazer referência à célula TxtPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5d3a-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e5d3a-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="e5d3a-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="e5d3a-112">Para fazer referência à célula TxtPinY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5d3a-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-113">Section index:</span></span>  <br/> |<span data-ttu-id="e5d3a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5d3a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e5d3a-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-115">Row index:</span></span>  <br/> |<span data-ttu-id="e5d3a-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="e5d3a-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="e5d3a-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e5d3a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e5d3a-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="e5d3a-118">**visXFormPinY**</span></span> <br/> |
   

