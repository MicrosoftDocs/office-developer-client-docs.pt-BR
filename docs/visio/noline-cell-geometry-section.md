---
title: Célula NoLine (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Determina se uma linha será desenhada em torno do limite do caminho.
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772410"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="cc63b-103">Célula NoLine (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="cc63b-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="cc63b-104">Determina se uma linha será desenhada em torno do limite do caminho.</span><span class="sxs-lookup"><span data-stu-id="cc63b-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="cc63b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cc63b-105">**Value**</span></span>|<span data-ttu-id="cc63b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc63b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cc63b-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="cc63b-107">TRUE</span></span>  <br/> | <span data-ttu-id="cc63b-108">Uma linha não é desenhada em torno do limite do caminho que é o limite de uma região preenchida.</span><span class="sxs-lookup"><span data-stu-id="cc63b-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="cc63b-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="cc63b-109">FALSE</span></span>  <br/> | <span data-ttu-id="cc63b-110">Uma linha é desenhada em torno do limite de um caminho.</span><span class="sxs-lookup"><span data-stu-id="cc63b-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc63b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc63b-111">Remarks</span></span>

<span data-ttu-id="cc63b-p101">Ao alterar a cor de uma linha para branca, a linha continuará a existir embora não seja possível visualizá-la em um plano de fundo branco. Se o valor da célula for definido para VERDADEIRO, nenhuma linha será desenhada.</span><span class="sxs-lookup"><span data-stu-id="cc63b-p101">When you change the color of a line to white, the line still exists even though you can't see it on a white background. When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="cc63b-114">Para obter uma referência à célula NoLine pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cc63b-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc63b-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cc63b-115">Cell name:</span></span>  <br/> | <span data-ttu-id="cc63b-116">Geometria *i* . NoLine onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cc63b-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cc63b-117">Para obter uma referência à célula NoLine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cc63b-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc63b-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cc63b-118">Section index:</span></span>  <br/> |<span data-ttu-id="cc63b-119">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cc63b-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cc63b-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cc63b-120">Row index:</span></span>  <br/> |<span data-ttu-id="cc63b-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="cc63b-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="cc63b-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cc63b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="cc63b-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="cc63b-123">**visCompNoLine**</span></span> <br/> |
   

