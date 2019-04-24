---
title: Célula Strikethru (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Determina se o texto está formatado como tachado.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349333"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="d5db6-103">Célula Strikethru (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="d5db6-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="d5db6-104">Determina se o texto está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="d5db6-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="d5db6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d5db6-105">**Value**</span></span>|<span data-ttu-id="d5db6-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d5db6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5db6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d5db6-107">TRUE</span></span>  <br/> |<span data-ttu-id="d5db6-108">O texto está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="d5db6-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="d5db6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d5db6-109">FALSE</span></span>  <br/> |<span data-ttu-id="d5db6-110">O texto não está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="d5db6-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5db6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5db6-111">Remarks</span></span>

<span data-ttu-id="d5db6-112">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="d5db6-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="d5db6-113">Para obter uma referência para a célula Strikethru pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d5db6-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5db6-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d5db6-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d5db6-115">Char. Strikethru [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d5db6-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d5db6-116">Para obter uma referência para a célula Strikethru pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d5db6-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5db6-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d5db6-117">Section index:</span></span>  <br/> |<span data-ttu-id="d5db6-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d5db6-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d5db6-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d5db6-119">Row index:</span></span>  <br/> |<span data-ttu-id="d5db6-120">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d5db6-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d5db6-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d5db6-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d5db6-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="d5db6-122">**visCharacterStrikethru**</span></span> <br/> |
   

