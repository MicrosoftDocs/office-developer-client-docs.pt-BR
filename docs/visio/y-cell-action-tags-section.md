---
title: Célula Y (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: Y-coordenar posição nas coordenadas locais da forma, em torno da qual é colocado o botão de marca de ação.
ms.openlocfilehash: 641c868703c6e4b0b7e749f68813b5869b5728c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773323"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="cfb06-103">Célula Y (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="cfb06-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="cfb06-104">*Y* -coordenar posição nas coordenadas locais da forma, em torno da qual é colocado o botão de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="cfb06-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cfb06-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="cfb06-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cfb06-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfb06-106">Remarks</span></span>

<span data-ttu-id="cfb06-107">As células X e Y definem um ponto nas coordenadas locais da forma, e as células X Justify e Y Justify definem o local em que o botão de marca de ação será colocado em relação àquele ponto.</span><span class="sxs-lookup"><span data-stu-id="cfb06-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="cfb06-108">Para obter uma referência à célula Y pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cfb06-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cfb06-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cfb06-109">Cell name:</span></span>  <br/> | <span data-ttu-id="cfb06-110">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="cfb06-110">SmartTags.</span></span>  <span data-ttu-id="cfb06-111">*nome* . Y onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="cfb06-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="cfb06-112">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="cfb06-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="cfb06-113">Para obter uma referência à célula Y pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cfb06-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cfb06-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cfb06-114">Section index:</span></span>  <br/> |<span data-ttu-id="cfb06-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="cfb06-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="cfb06-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cfb06-116">Row index:</span></span>  <br/> |<span data-ttu-id="cfb06-117">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cfb06-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cfb06-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cfb06-118">Cell index:</span></span>  <br/> |<span data-ttu-id="cfb06-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="cfb06-119">**visSmartTagY**</span></span> <br/> |
   

