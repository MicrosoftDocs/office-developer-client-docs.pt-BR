---
title: Célula NoQuickDrag (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Determina se uma forma pode ser selecionada ou arrastada quando o usuário clica na área preenchida definida pela seção Geometry.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772424"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="96b4b-103">Célula NoQuickDrag (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="96b4b-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="96b4b-104">Determina se uma forma pode ser selecionada ou arrastada quando o usuário clica na área preenchida definida pela seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="96b4b-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96b4b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="96b4b-105">Remarks</span></span>

<span data-ttu-id="96b4b-106">Para obter uma referência à célula NoQuickDrag pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="96b4b-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96b4b-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="96b4b-107">Cell name:</span></span>  <br/> |<span data-ttu-id="96b4b-108">Geometria *i* . NoQuickDrag, onde * i * - < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="96b4b-108">Geometry  *i*  .NoQuickDrag, where  * i *  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="96b4b-109">Para obter uma referência à célula NoQuickDrag pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="96b4b-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96b4b-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="96b4b-110">Section index:</span></span>  <br/> |<span data-ttu-id="96b4b-111">**visSectionFirstComponent** +  *i* , onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="96b4b-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="96b4b-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="96b4b-112">Row index:</span></span>  <br/> |<span data-ttu-id="96b4b-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="96b4b-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="96b4b-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="96b4b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="96b4b-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="96b4b-115">**visCompNoQuickDrag**</span></span> <br/> |
   

