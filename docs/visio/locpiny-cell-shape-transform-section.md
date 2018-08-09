---
title: Célula LocPinY (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Representa o y-coordenadas do pino da forma (Centro de rotação) em relação à origem da forma. A fórmula padrão para determinar LocPinY é:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772281"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="1190e-104">Célula LocPinY (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="1190e-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="1190e-105">Representa o *y* -coordenadas do pino da forma (Centro de rotação) em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="1190e-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="1190e-106">A fórmula padrão para determinar LocPinY é:</span><span class="sxs-lookup"><span data-stu-id="1190e-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="1190e-107">= A altura \* 0.5</span><span class="sxs-lookup"><span data-stu-id="1190e-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1190e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1190e-108">Remarks</span></span>

<span data-ttu-id="1190e-109">Para fazer referência à célula LocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="1190e-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1190e-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1190e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="1190e-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="1190e-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="1190e-112">Para fazer referência à célula LocPinY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1190e-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1190e-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1190e-113">Section index:</span></span>  <br/> |<span data-ttu-id="1190e-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1190e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1190e-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1190e-115">Row index:</span></span>  <br/> |<span data-ttu-id="1190e-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="1190e-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="1190e-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1190e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="1190e-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="1190e-118">**visXFormLocPinY**</span></span> <br/> |
   

