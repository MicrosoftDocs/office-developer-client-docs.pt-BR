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
description: Uma célula de evento que é avaliada quando a posição de uma forma ou orientação na página é transformado (XF).
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771842"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="0fc08-103">Célula EventXFMod (Seção Events)</span><span class="sxs-lookup"><span data-stu-id="0fc08-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="0fc08-104">Uma célula de evento avaliada ao transformar uma posição da forma ou orientação na página ("XF").</span><span class="sxs-lookup"><span data-stu-id="0fc08-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fc08-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fc08-105">Remarks</span></span>

<span data-ttu-id="0fc08-106">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="0fc08-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="0fc08-107">Para fazer referência à célula EventXFMod pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0fc08-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fc08-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0fc08-108">Cell name:</span></span>  <br/> | <span data-ttu-id="0fc08-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="0fc08-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="0fc08-110">Para fazer referência à célula EventXFMod pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0fc08-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fc08-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0fc08-111">Section index:</span></span>  <br/> |<span data-ttu-id="0fc08-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0fc08-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0fc08-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0fc08-113">Row index:</span></span>  <br/> |<span data-ttu-id="0fc08-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="0fc08-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="0fc08-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0fc08-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0fc08-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="0fc08-116">**visEvtCellXFMod**</span></span> <br/> |
   

