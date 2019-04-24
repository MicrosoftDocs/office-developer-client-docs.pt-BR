---
title: Célula X (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: A posição da coordenada x nas coordenadas locais da forma em torno da qual o botão de marca de ação é colocado.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335765"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="61385-103">Célula X (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="61385-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="61385-104">A posição da coordenada *x* nas coordenadas locais da forma em torno da qual o botão de marca de ação é colocado.</span><span class="sxs-lookup"><span data-stu-id="61385-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="61385-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="61385-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61385-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="61385-106">Remarks</span></span>

<span data-ttu-id="61385-107">As células X e Y definem um ponto nas coordenadas locais da forma, e as células X Justify e Y Justify definem o local em que o botão de marca de ação será colocado em relação àquele ponto.</span><span class="sxs-lookup"><span data-stu-id="61385-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="61385-108">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="61385-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61385-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="61385-109">Cell name:</span></span>  <br/> |<span data-ttu-id="61385-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="61385-110">SmartTags.</span></span> <span data-ttu-id="61385-111">*nome* . X em que SmartTags.</span><span class="sxs-lookup"><span data-stu-id="61385-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="61385-112">*name*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="61385-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="61385-113">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="61385-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61385-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="61385-114">Section index:</span></span>  <br/> |<span data-ttu-id="61385-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="61385-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="61385-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="61385-116">Row index:</span></span>  <br/> |<span data-ttu-id="61385-117">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="61385-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="61385-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="61385-118">Cell index:</span></span>  <br/> |<span data-ttu-id="61385-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="61385-119">**visSmartTagX**</span></span> <br/> |
   

