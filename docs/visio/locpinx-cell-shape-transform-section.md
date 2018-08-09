---
title: Célula LocPinX (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Representa o x-coordenadas do pino da forma (Centro de rotação) em relação à origem da forma. A fórmula padrão para determinar LocPinX é:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772294"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="4d4eb-104">Célula LocPinX (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="4d4eb-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="4d4eb-105">Representa o *x* -coordenadas do pino da forma (Centro de rotação) em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="4d4eb-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="4d4eb-106">A fórmula padrão para determinar LocPinX é:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="4d4eb-107">= A largura \* 0.5</span><span class="sxs-lookup"><span data-stu-id="4d4eb-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d4eb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d4eb-108">Remarks</span></span>

<span data-ttu-id="4d4eb-109">Para fazer referência à célula LocPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d4eb-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-110">Cell name:</span></span>  <br/> | <span data-ttu-id="4d4eb-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="4d4eb-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="4d4eb-112">Para fazer referência à célula LocPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d4eb-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-113">Section index:</span></span>  <br/> |<span data-ttu-id="4d4eb-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d4eb-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4d4eb-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-115">Row index:</span></span>  <br/> |<span data-ttu-id="4d4eb-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="4d4eb-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="4d4eb-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4d4eb-117">Cell index:</span></span>  <br/> |<span data-ttu-id="4d4eb-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="4d4eb-118">**visXFormLocPinX**</span></span> <br/> |
   

