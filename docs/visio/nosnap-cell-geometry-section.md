---
title: Célula NoSnap (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Determina se outras formas se ajustarão a um caminho.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408541"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="5be2b-103">Célula NoSnap (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="5be2b-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="5be2b-104">Determina se outras formas se ajustarão a um caminho.</span><span class="sxs-lookup"><span data-stu-id="5be2b-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="5be2b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5be2b-105">**Value**</span></span>|<span data-ttu-id="5be2b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5be2b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5be2b-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="5be2b-107">TRUE</span></span>  <br/> | <span data-ttu-id="5be2b-108">Não permitir que outras formas sejam ajustadas a este caminho.</span><span class="sxs-lookup"><span data-stu-id="5be2b-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="5be2b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5be2b-109">FALSE</span></span>  <br/> | <span data-ttu-id="5be2b-110">Permitir que outras formas sejam ajustadas a este caminho.</span><span class="sxs-lookup"><span data-stu-id="5be2b-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5be2b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5be2b-111">Remarks</span></span>

<span data-ttu-id="5be2b-112">Para fazer referência à célula NoSnap pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="5be2b-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5be2b-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5be2b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5be2b-114">Geometry *i* . NoSnap onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5be2b-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5be2b-115">Para fazer referência à célula NoSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5be2b-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5be2b-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5be2b-116">Section index:</span></span>  <br/> |<span data-ttu-id="5be2b-117">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5be2b-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5be2b-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5be2b-118">Row index:</span></span>  <br/> |<span data-ttu-id="5be2b-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="5be2b-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="5be2b-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5be2b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5be2b-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="5be2b-121">**visCompNoSnap**</span></span> <br/> |
   

