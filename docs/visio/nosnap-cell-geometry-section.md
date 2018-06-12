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
description: Determina se outras formas serão ajustadas a um caminho.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772425"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="8bd2e-103">Célula NoSnap (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="8bd2e-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="8bd2e-104">Determina se outras formas serão ajustadas a um caminho.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="8bd2e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8bd2e-105">**Value**</span></span>|<span data-ttu-id="8bd2e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8bd2e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8bd2e-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="8bd2e-107">TRUE</span></span>  <br/> | <span data-ttu-id="8bd2e-108">Não permitir que outras formas sejam ajustadas a este caminho.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="8bd2e-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="8bd2e-109">FALSE</span></span>  <br/> | <span data-ttu-id="8bd2e-110">Permitir que outras formas sejam ajustadas a este caminho.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bd2e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bd2e-111">Remarks</span></span>

<span data-ttu-id="8bd2e-112">Para obter uma referência à célula NoSnap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="8bd2e-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8bd2e-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8bd2e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8bd2e-114">Geometria *i* . NoSnap onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8bd2e-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8bd2e-115">Para obter uma referência à célula NoSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8bd2e-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8bd2e-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8bd2e-116">Section index:</span></span>  <br/> |<span data-ttu-id="8bd2e-117">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8bd2e-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8bd2e-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8bd2e-118">Row index:</span></span>  <br/> |<span data-ttu-id="8bd2e-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="8bd2e-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="8bd2e-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8bd2e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8bd2e-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="8bd2e-121">**visCompNoSnap**</span></span> <br/> |
   

