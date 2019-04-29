---
title: Célula TxtHeight (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Determina a altura do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409304"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="b6c89-104">Célula TxtHeight (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="b6c89-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="b6c89-105">Determina a altura do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="b6c89-105">Determines the height of the text block.</span></span> <span data-ttu-id="b6c89-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="b6c89-106">The default formula is:</span></span>
  
<span data-ttu-id="b6c89-107">= Altura \* 1</span><span class="sxs-lookup"><span data-stu-id="b6c89-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6c89-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c89-108">Remarks</span></span>

<span data-ttu-id="b6c89-109">Para fazer referência à célula TxtHeight pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b6c89-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6c89-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b6c89-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b6c89-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="b6c89-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="b6c89-112">Para fazer referência à célula TxtHeight pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b6c89-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6c89-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b6c89-113">Section index:</span></span>  <br/> |<span data-ttu-id="b6c89-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6c89-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b6c89-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b6c89-115">Row index:</span></span>  <br/> |<span data-ttu-id="b6c89-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="b6c89-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="b6c89-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b6c89-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b6c89-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="b6c89-118">**visXFormHeight**</span></span> <br/> |
   

