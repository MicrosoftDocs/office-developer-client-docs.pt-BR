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
description: 'Determina o x-coordenadas do centro do bloco de texto de rotação em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773182"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="0ed1d-104">Célula TxtLocPinX (seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="0ed1d-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="0ed1d-105">Determina o *x* -coordenadas do centro do bloco de texto de rotação em relação à origem do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="0ed1d-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-106">The default formula is:</span></span> 
  
<span data-ttu-id="0ed1d-107">= TxtWidth \* 0.5</span><span class="sxs-lookup"><span data-stu-id="0ed1d-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="0ed1d-108">Essa fórmula avalia o centro horizontal do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ed1d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ed1d-109">Remarks</span></span>

<span data-ttu-id="0ed1d-110">Para obter uma referência à célula TxtLocPinX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ed1d-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="0ed1d-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="0ed1d-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="0ed1d-113">Para obter uma referência à célula TxtLocPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ed1d-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-114">Section index:</span></span>  <br/> |<span data-ttu-id="0ed1d-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ed1d-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0ed1d-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-116">Row index:</span></span>  <br/> |<span data-ttu-id="0ed1d-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="0ed1d-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="0ed1d-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="0ed1d-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="0ed1d-119">**visXFormLocPinX**</span></span> <br/> |
   

