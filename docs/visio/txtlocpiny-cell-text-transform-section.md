---
title: Célula TxtLocPinY (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Determina a coordenada y do centro de rotação do bloco de texto em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317728"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="51e36-104">Célula TxtLocPinY (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="51e36-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="51e36-105">Determina a coordenada *y* do centro de rotação do bloco de texto em relação à origem do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="51e36-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="51e36-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="51e36-106">The default formula is:</span></span> 
  
<span data-ttu-id="51e36-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="51e36-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51e36-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="51e36-108">Remarks</span></span>

<span data-ttu-id="51e36-109">Para fazer referência à célula TxtLocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="51e36-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51e36-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="51e36-110">Cell name:</span></span>  <br/> | <span data-ttu-id="51e36-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="51e36-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="51e36-112">Para fazer referência à célula TxtLocPinY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="51e36-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51e36-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="51e36-113">Section index:</span></span>  <br/> |<span data-ttu-id="51e36-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51e36-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51e36-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="51e36-115">Row index:</span></span>  <br/> |<span data-ttu-id="51e36-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="51e36-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="51e36-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="51e36-117">Cell index:</span></span>  <br/> |<span data-ttu-id="51e36-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="51e36-118">**visXFormLocPinY**</span></span> <br/> |
   

