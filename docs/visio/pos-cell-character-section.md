---
title: Célula Pos (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Determina a posição do texto da forma em relação à linha de base.
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772583"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="88675-103">Célula Pos (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="88675-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="88675-104">Determina a posição do texto da forma em relação à linha de base.</span><span class="sxs-lookup"><span data-stu-id="88675-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="88675-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="88675-105">**Value**</span></span>|<span data-ttu-id="88675-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="88675-106">**Description**</span></span>|<span data-ttu-id="88675-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="88675-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="88675-108">0</span><span class="sxs-lookup"><span data-stu-id="88675-108">0</span></span>  <br/> | <span data-ttu-id="88675-109">Posição normal</span><span class="sxs-lookup"><span data-stu-id="88675-109">Normal position</span></span>  <br/> |<span data-ttu-id="88675-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="88675-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="88675-111">1</span><span class="sxs-lookup"><span data-stu-id="88675-111">1</span></span>  <br/> | <span data-ttu-id="88675-112">Sobrescrito</span><span class="sxs-lookup"><span data-stu-id="88675-112">Superscript</span></span>  <br/> |<span data-ttu-id="88675-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="88675-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="88675-114">2</span><span class="sxs-lookup"><span data-stu-id="88675-114">2</span></span>  <br/> | <span data-ttu-id="88675-115">Subscrito</span><span class="sxs-lookup"><span data-stu-id="88675-115">Subscript</span></span>  <br/> |<span data-ttu-id="88675-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="88675-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88675-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="88675-117">Remarks</span></span>

<span data-ttu-id="88675-118">Para fazer referência à célula Pos pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="88675-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88675-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="88675-119">Cell name:</span></span>  <br/> | <span data-ttu-id="88675-120">Char.Pos [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="88675-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="88675-121">Para fazer referência à célula Pos pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="88675-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88675-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="88675-122">Section index:</span></span>  <br/> |<span data-ttu-id="88675-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="88675-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="88675-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="88675-124">Row index:</span></span>  <br/> |<span data-ttu-id="88675-125">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="88675-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="88675-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="88675-126">Cell index:</span></span>  <br/> |<span data-ttu-id="88675-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="88675-127">**visCharacterPos**</span></span> <br/> |
   

