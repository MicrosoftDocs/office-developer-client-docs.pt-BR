---
title: Célula EventDrop (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Uma célula de evento avaliada ao soltar uma forma na página de desenho, como uma instância ou ao duplicar ou colar uma forma.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351006"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="dcbbd-103">Célula EventDrop (Seção Events)</span><span class="sxs-lookup"><span data-stu-id="dcbbd-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="dcbbd-104">Uma célula de evento avaliada ao soltar uma forma na página de desenho, como uma instância ou ao duplicar ou colar uma forma.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dcbbd-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcbbd-105">Remarks</span></span>

<span data-ttu-id="dcbbd-106">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="dcbbd-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="dcbbd-107">Para fazer referência à célula EventDrop pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="dcbbd-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcbbd-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="dcbbd-108">Cell name:</span></span>  <br/> | <span data-ttu-id="dcbbd-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="dcbbd-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="dcbbd-110">Para fazer referência à célula EventDrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="dcbbd-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcbbd-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="dcbbd-111">Section index:</span></span>  <br/> |<span data-ttu-id="dcbbd-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dcbbd-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dcbbd-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="dcbbd-113">Row index:</span></span>  <br/> |<span data-ttu-id="dcbbd-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="dcbbd-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="dcbbd-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="dcbbd-115">Cell index:</span></span>  <br/> |<span data-ttu-id="dcbbd-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="dcbbd-116">**visEvtCellDrop**</span></span> <br/> |
   

