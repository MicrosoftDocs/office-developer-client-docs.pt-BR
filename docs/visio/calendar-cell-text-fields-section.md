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
description: Determina o calendário a ser usado para um campo de texto quando o tipo de dado for Data.
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424746"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="66ad5-103">Célula Calendar (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="66ad5-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="66ad5-104">Determina o calendário a ser usado para um campo de texto quando o tipo de dado for Data.</span><span class="sxs-lookup"><span data-stu-id="66ad5-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66ad5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="66ad5-105">Remarks</span></span>

<span data-ttu-id="66ad5-106">Os valores possíveis são: 0 (Ocidental), 1 (Islâmico árabe), 2 (Lunar hebraico), 3 (Calendário de Taiwan), 4 (Reinado do imperador japonês), 5 (Budista tailandês), 6 (Danki coreano), 7 (Era Saka), 8 (Transliteração inglesa) e 9 (Transliteração francesa).</span><span class="sxs-lookup"><span data-stu-id="66ad5-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="66ad5-107">Para fazer referência à célula Calendar pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="66ad5-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66ad5-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="66ad5-108">Cell name:</span></span>  <br/> | <span data-ttu-id="66ad5-109">Fields.Calendar[  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="66ad5-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="66ad5-110">Para fazer referência à célula Calendar pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="66ad5-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66ad5-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="66ad5-111">Section index:</span></span>  <br/> |<span data-ttu-id="66ad5-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="66ad5-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="66ad5-113">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="66ad5-113">Row index:</span></span>  <br/> |<span data-ttu-id="66ad5-114">**visRowField**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="66ad5-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="66ad5-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="66ad5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="66ad5-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="66ad5-116">**visFieldCalendar**</span></span> <br/> |
   

