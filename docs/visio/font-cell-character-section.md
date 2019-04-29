---
title: Célula Font (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Representa o número da fonte utilizada para formatar o texto. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. O número 0 representa a fonte padrão, normalmente Arial.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438663"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="3cd5d-105">Célula Font (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="3cd5d-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="3cd5d-p102">Representa o número da fonte utilizada para formatar o texto. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. O número 0 representa a fonte padrão, normalmente Arial.</span><span class="sxs-lookup"><span data-stu-id="3cd5d-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3cd5d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd5d-109">Remarks</span></span>

<span data-ttu-id="3cd5d-110">Para fazer referência à célula Font pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3cd5d-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3cd5d-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3cd5d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="3cd5d-112">Char. Font [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3cd5d-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3cd5d-113">Para fazer referência à célula Font pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3cd5d-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3cd5d-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3cd5d-114">Section index:</span></span>  <br/> |<span data-ttu-id="3cd5d-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="3cd5d-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="3cd5d-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3cd5d-116">Row index:</span></span>  <br/> |<span data-ttu-id="3cd5d-117">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3cd5d-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3cd5d-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3cd5d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="3cd5d-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="3cd5d-119">**visCharacterFont**</span></span> <br/> |
   

