---
title: Célula EventDblClick (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Uma célula de evento avaliada ao se clicar duas vezes em uma forma.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337167"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="ddeb5-103">Célula EventDblClick (Seção Events)</span><span class="sxs-lookup"><span data-stu-id="ddeb5-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="ddeb5-104">Uma célula de evento avaliada ao se clicar duas vezes em uma forma.</span><span class="sxs-lookup"><span data-stu-id="ddeb5-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddeb5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddeb5-105">Remarks</span></span>

<span data-ttu-id="ddeb5-106">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="ddeb5-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="ddeb5-107">Para fazer referência à célula EventDblClick pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ddeb5-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddeb5-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ddeb5-108">Cell name:</span></span>  <br/> | <span data-ttu-id="ddeb5-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="ddeb5-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="ddeb5-110">Para fazer referência à célula EventDblClick pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ddeb5-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddeb5-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ddeb5-111">Section index:</span></span>  <br/> |<span data-ttu-id="ddeb5-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddeb5-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ddeb5-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ddeb5-113">Row index:</span></span>  <br/> |<span data-ttu-id="ddeb5-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="ddeb5-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="ddeb5-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ddeb5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ddeb5-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="ddeb5-116">**visEvtCellDblClick**</span></span> <br/> |
   

