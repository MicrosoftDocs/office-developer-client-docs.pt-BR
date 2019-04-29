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
description: 'Representa a coordenada x do pino da forma (centro de rotação) em relação à origem da forma. A fórmula padrão para determinar a célula LocPinX é:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439237"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="91cf7-104">Célula LocPinX (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="91cf7-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="91cf7-105">Representa a coordenada *x* do pino da forma (centro de rotação) em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="91cf7-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="91cf7-106">A fórmula padrão para determinar a célula LocPinX é:</span><span class="sxs-lookup"><span data-stu-id="91cf7-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="91cf7-107">= Largura \* 0,5</span><span class="sxs-lookup"><span data-stu-id="91cf7-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91cf7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="91cf7-108">Remarks</span></span>

<span data-ttu-id="91cf7-109">Para fazer referência à célula LocPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="91cf7-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91cf7-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="91cf7-110">Cell name:</span></span>  <br/> | <span data-ttu-id="91cf7-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="91cf7-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="91cf7-112">Para fazer referência à célula LocPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="91cf7-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91cf7-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="91cf7-113">Section index:</span></span>  <br/> |<span data-ttu-id="91cf7-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91cf7-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="91cf7-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="91cf7-115">Row index:</span></span>  <br/> |<span data-ttu-id="91cf7-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="91cf7-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="91cf7-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="91cf7-117">Cell index:</span></span>  <br/> |<span data-ttu-id="91cf7-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="91cf7-118">**visXFormLocPinX**</span></span> <br/> |
   

