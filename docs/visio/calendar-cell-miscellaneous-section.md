---
title: Célula Calendar (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Determina o calendário a ser usado quando a fórmula de uma célula contém informações de Data.
ms.openlocfilehash: 2bca91fd2efc283bcc8f2c5037c4d81dd9bcffc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771427"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="c7ffb-103">Célula Calendar (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="c7ffb-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c7ffb-104">Determina o calendário a ser usado quando a fórmula de uma célula contém informações de Data.</span><span class="sxs-lookup"><span data-stu-id="c7ffb-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7ffb-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ffb-105">Remarks</span></span>

<span data-ttu-id="c7ffb-106">Os valores possíveis são: 0 (Ocidental), 1 (Islâmico árabe), 2 (Lunar hebraico), 3 (Calendário de Taiwan), 4 (Reinado do imperador japonês), 5 (Budista tailandês), 6 (Danki coreano), 7 (Era Saka), 8 (Transliteração inglesa) e 9 (Transliteração francesa).</span><span class="sxs-lookup"><span data-stu-id="c7ffb-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="c7ffb-107">Para obter uma referência à célula Calendar pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c7ffb-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7ffb-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c7ffb-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c7ffb-109">Calendar</span><span class="sxs-lookup"><span data-stu-id="c7ffb-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="c7ffb-110">Para obter uma referência à célula Calendar pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c7ffb-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7ffb-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c7ffb-111">Section index:</span></span>  <br/> |<span data-ttu-id="c7ffb-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7ffb-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7ffb-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c7ffb-113">Row index:</span></span>  <br/> |<span data-ttu-id="c7ffb-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c7ffb-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c7ffb-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c7ffb-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c7ffb-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="c7ffb-116">**visObjCalendar**</span></span> <br/> |
   

