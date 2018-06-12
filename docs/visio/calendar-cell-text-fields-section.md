---
title: Célula Calendar (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Determina o calendário que é usado para um campo de texto quando o tipo de dado for Data.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771417"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="1e5ff-103">Célula Calendar (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="1e5ff-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="1e5ff-104">Determina o calendário que é usado para um campo de texto quando o tipo de dado for Data.</span><span class="sxs-lookup"><span data-stu-id="1e5ff-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e5ff-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e5ff-105">Remarks</span></span>

<span data-ttu-id="1e5ff-106">Os valores possíveis são: 0 (Ocidental), 1 (Islâmico árabe), 2 (Lunar hebraico), 3 (Calendário de Taiwan), 4 (Reinado do imperador japonês), 5 (Budista tailandês), 6 (Danki coreano), 7 (Era Saka), 8 (Transliteração inglesa) e 9 (Transliteração francesa).</span><span class="sxs-lookup"><span data-stu-id="1e5ff-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="1e5ff-107">Para obter uma referência à célula Calendar pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="1e5ff-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e5ff-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1e5ff-108">Cell name:</span></span>  <br/> | <span data-ttu-id="1e5ff-109">Fields.Calendar [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1e5ff-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1e5ff-110">Para obter uma referência à célula Calendar pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1e5ff-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e5ff-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1e5ff-111">Section index:</span></span>  <br/> |<span data-ttu-id="1e5ff-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="1e5ff-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="1e5ff-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1e5ff-113">Row index:</span></span>  <br/> |<span data-ttu-id="1e5ff-114">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1e5ff-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1e5ff-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1e5ff-115">Cell index:</span></span>  <br/> |<span data-ttu-id="1e5ff-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="1e5ff-116">**visFieldCalendar**</span></span> <br/> |
   

