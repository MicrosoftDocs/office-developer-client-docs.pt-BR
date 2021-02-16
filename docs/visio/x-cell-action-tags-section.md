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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431110"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="3b32a-103">Célula X (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="3b32a-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="3b32a-104">A  *posição da*  coordenada x nas coordenadas locais da forma em torno da qual o botão de marca de ação é colocado.</span><span class="sxs-lookup"><span data-stu-id="3b32a-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b32a-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="3b32a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b32a-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b32a-106">Remarks</span></span>

<span data-ttu-id="3b32a-107">As células X e Y definem um ponto nas coordenadas locais da forma, e as células X Justify e Y Justify definem o local em que o botão de marca de ação será colocado em relação àquele ponto.</span><span class="sxs-lookup"><span data-stu-id="3b32a-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="3b32a-108">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3b32a-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b32a-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3b32a-109">Cell name:</span></span>  <br/> |<span data-ttu-id="3b32a-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3b32a-110">SmartTags.</span></span> <span data-ttu-id="3b32a-111">*nome*  . X onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3b32a-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="3b32a-112">*nome*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="3b32a-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3b32a-113">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3b32a-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b32a-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3b32a-114">Section index:</span></span>  <br/> |<span data-ttu-id="3b32a-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3b32a-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3b32a-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3b32a-116">Row index:</span></span>  <br/> |<span data-ttu-id="3b32a-117">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3b32a-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3b32a-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3b32a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="3b32a-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="3b32a-119">**visSmartTagX**</span></span> <br/> |
   

