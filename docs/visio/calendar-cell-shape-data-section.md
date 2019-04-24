---
title: Célula Calendar (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Determina o calendário que é usado para dados da forma quando o tipo de dados é Data.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337503"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="14d67-103">Célula Calendar (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="14d67-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="14d67-104">Determina o calendário que é usado para dados da forma quando o tipo de dados é Data.</span><span class="sxs-lookup"><span data-stu-id="14d67-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14d67-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="14d67-105">Remarks</span></span>

<span data-ttu-id="14d67-106">Os valores possíveis são: 0 (Ocidental), 1 (Islâmico árabe), 2 (Lunar hebraico), 3 (Calendário de Taiwan), 4 (Reinado do imperador japonês), 5 (Budista tailandês), 6 (Danki coreano), 7 (Era Saka), 8 (Transliteração inglesa) e 9 (Transliteração francesa).</span><span class="sxs-lookup"><span data-stu-id="14d67-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="14d67-107">Para fazer referência à célula Calendar pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="14d67-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14d67-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="14d67-108">Cell name:</span></span>  <br/> | <span data-ttu-id="14d67-109">Hélice.  *nome* . Calendário em que prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="14d67-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="14d67-110">Para fazer referência à célula Calendar pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="14d67-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14d67-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="14d67-111">Section index:</span></span>  <br/> |<span data-ttu-id="14d67-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="14d67-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="14d67-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="14d67-113">Row index:</span></span>  <br/> |<span data-ttu-id="14d67-114">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="14d67-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="14d67-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="14d67-115">Cell index:</span></span>  <br/> |<span data-ttu-id="14d67-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="14d67-116">**visCustPropsCalendar**</span></span> <br/> |
   

