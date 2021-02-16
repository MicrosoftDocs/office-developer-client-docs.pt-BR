---
title: Célula NoFill (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indica se um caminho pode ser preenchido.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415016"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="ceb24-103">Célula NoFill (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="ceb24-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="ceb24-104">Indica se um caminho pode ser preenchido.</span><span class="sxs-lookup"><span data-stu-id="ceb24-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="ceb24-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ceb24-105">**Value**</span></span>|<span data-ttu-id="ceb24-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ceb24-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ceb24-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="ceb24-107">TRUE</span></span>  <br/> | <span data-ttu-id="ceb24-108">O caminho não é preenchido mesmo se outros caminhos da forma forem preenchidos.</span><span class="sxs-lookup"><span data-stu-id="ceb24-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="ceb24-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ceb24-109">FALSE</span></span>  <br/> | <span data-ttu-id="ceb24-110">O preenchimento da forma é aplicado ao caminho, mesmo se não estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="ceb24-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ceb24-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceb24-111">Remarks</span></span>

<span data-ttu-id="ceb24-p101">Se você definir o padrão de preenchimento de uma forma para nenhum (0), nenhum de seus caminhos serão preenchidos. Esta célula é utilizada para desativar seletivamente o preenchimento do caminho em uma forma.</span><span class="sxs-lookup"><span data-stu-id="ceb24-p101">If you set a shape's fill pattern to none (0), none of its paths are filled. This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="ceb24-114">Para fazer referência à célula NoFill pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ceb24-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ceb24-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ceb24-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ceb24-116">Geometry  *i*  . NoFill onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ceb24-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ceb24-117">Para fazer referência à célula NoFill pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ceb24-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ceb24-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ceb24-118">Section index:</span></span>  <br/> |<span data-ttu-id="ceb24-119">**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ceb24-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ceb24-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ceb24-120">Row index:</span></span>  <br/> |<span data-ttu-id="ceb24-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="ceb24-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="ceb24-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ceb24-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ceb24-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="ceb24-123">**visCompNoFill**</span></span> <br/> |
   

