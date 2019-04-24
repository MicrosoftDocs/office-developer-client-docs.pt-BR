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
description: 'Representa a coordenada y do pino da forma (centro de rotação) em relação à origem da forma. A fórmula padrão para determinar a célula LocPinY é:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358041"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="b5363-104">Célula LocPinY (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="b5363-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="b5363-105">Representa a coordenada *y* do pino da forma (centro de rotação) em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="b5363-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="b5363-106">A fórmula padrão para determinar a célula LocPinY é:</span><span class="sxs-lookup"><span data-stu-id="b5363-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="b5363-107">= Altura \* 0,5</span><span class="sxs-lookup"><span data-stu-id="b5363-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5363-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5363-108">Remarks</span></span>

<span data-ttu-id="b5363-109">Para fazer referência à célula LocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b5363-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5363-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b5363-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b5363-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="b5363-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="b5363-112">Para fazer referência à célula LocPinY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b5363-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5363-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b5363-113">Section index:</span></span>  <br/> |<span data-ttu-id="b5363-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5363-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b5363-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b5363-115">Row index:</span></span>  <br/> |<span data-ttu-id="b5363-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="b5363-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="b5363-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b5363-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b5363-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="b5363-118">**visXFormLocPinY**</span></span> <br/> |
   

