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
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771770"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="b63c2-103">Célula DoubleStrikethrough (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="b63c2-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="b63c2-104">Determina se o texto será formatado como tachado duplo.</span><span class="sxs-lookup"><span data-stu-id="b63c2-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b63c2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b63c2-105">Remarks</span></span>

<span data-ttu-id="b63c2-106">Para fazer referência à célula DoubleStrikethrough pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b63c2-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b63c2-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b63c2-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b63c2-108">Char.DoubleStrikethrough [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b63c2-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b63c2-109">Para fazer referência à célula DoubleStrikethrough pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b63c2-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b63c2-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b63c2-110">Section index:</span></span>  <br/> |<span data-ttu-id="b63c2-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b63c2-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="b63c2-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b63c2-112">Row index:</span></span>  <br/> |<span data-ttu-id="b63c2-113">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b63c2-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b63c2-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b63c2-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b63c2-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="b63c2-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

