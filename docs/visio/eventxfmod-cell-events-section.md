---
title: Célula EventXFMod (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Uma célula de evento que é avaliada quando a posição ou a orientação de uma forma na página é transformada (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350971"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="d0a0b-103">Célula EventXFMod (Seção Events)</span><span class="sxs-lookup"><span data-stu-id="d0a0b-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="d0a0b-104">Uma célula de evento avaliada ao transformar uma posição da forma ou orientação na página ("XF").</span><span class="sxs-lookup"><span data-stu-id="d0a0b-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0a0b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0a0b-105">Remarks</span></span>

<span data-ttu-id="d0a0b-106">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="d0a0b-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="d0a0b-107">Para fazer referência à célula EventXFMod pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d0a0b-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0a0b-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d0a0b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d0a0b-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="d0a0b-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="d0a0b-110">Para fazer referência à célula EventXFMod pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d0a0b-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0a0b-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d0a0b-111">Section index:</span></span>  <br/> |<span data-ttu-id="d0a0b-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d0a0b-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d0a0b-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d0a0b-113">Row index:</span></span>  <br/> |<span data-ttu-id="d0a0b-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="d0a0b-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="d0a0b-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d0a0b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d0a0b-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="d0a0b-116">**visEvtCellXFMod**</span></span> <br/> |
   

