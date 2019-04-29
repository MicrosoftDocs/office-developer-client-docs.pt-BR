---
title: Célula DoubleStrikethrough (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Determina se o texto será formatado como tachado duplo.
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360589"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="042c1-103">Célula DoubleStrikethrough (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="042c1-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="042c1-104">Determina se o texto será formatado como tachado duplo.</span><span class="sxs-lookup"><span data-stu-id="042c1-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="042c1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="042c1-105">Remarks</span></span>

<span data-ttu-id="042c1-106">Para fazer referência à célula DoubleStrikethrough pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="042c1-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="042c1-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="042c1-107">Cell name:</span></span>  <br/> | <span data-ttu-id="042c1-108">Char.DoubleStrikethrough[  *i*  ]            onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="042c1-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="042c1-109">Para fazer referência à célula DoubleStrikethrough pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="042c1-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="042c1-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="042c1-110">Section index:</span></span>  <br/> |<span data-ttu-id="042c1-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="042c1-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="042c1-112">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="042c1-112">Row index:</span></span>  <br/> |<span data-ttu-id="042c1-113">**visRowCharacter** +  *i*            onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="042c1-113">**visRowCharacter** +  +  \*\* 
          where *i* = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="042c1-114">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="042c1-114">Cell index:</span></span>  <br/> |<span data-ttu-id="042c1-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="042c1-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

