---
title: Célula TxtLocPinX (seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Determina a coordenada x do centro de rotação do bloco de texto em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425852"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="633f3-104">Célula TxtLocPinX (seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="633f3-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="633f3-105">Determina a coordenada *x* do centro de rotação do bloco de texto em relação à origem do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="633f3-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="633f3-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="633f3-106">The default formula is:</span></span> 
  
<span data-ttu-id="633f3-107">= TxtWidth \* 0,5</span><span class="sxs-lookup"><span data-stu-id="633f3-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="633f3-108">Essa fórmula avalia o centro horizontal do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="633f3-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="633f3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="633f3-109">Remarks</span></span>

<span data-ttu-id="633f3-110">Para fazer referência à célula TxtLocPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="633f3-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="633f3-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="633f3-111">Cell name:</span></span>  <br/> | <span data-ttu-id="633f3-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="633f3-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="633f3-113">Para fazer referência à célula TxtLocPinX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="633f3-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="633f3-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="633f3-114">Section index:</span></span>  <br/> |<span data-ttu-id="633f3-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="633f3-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="633f3-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="633f3-116">Row index:</span></span>  <br/> |<span data-ttu-id="633f3-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="633f3-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="633f3-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="633f3-118">Cell index:</span></span>  <br/> |<span data-ttu-id="633f3-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="633f3-119">**visXFormLocPinX**</span></span> <br/> |
   

