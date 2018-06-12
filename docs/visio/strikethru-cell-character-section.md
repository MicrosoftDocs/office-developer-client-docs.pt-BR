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
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773077"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="cbb88-103">Célula Strikethru (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="cbb88-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="cbb88-104">Determina se o texto está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="cbb88-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cbb88-105">**Value**</span></span>|<span data-ttu-id="cbb88-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbb88-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbb88-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="cbb88-107">TRUE</span></span>  <br/> |<span data-ttu-id="cbb88-108">O texto está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="cbb88-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="cbb88-109">FALSE</span></span>  <br/> |<span data-ttu-id="cbb88-110">O texto não está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbb88-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbb88-111">Remarks</span></span>

<span data-ttu-id="cbb88-112">Você também pode definir o valor desta célula usando a caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ).</span><span class="sxs-lookup"><span data-stu-id="cbb88-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="cbb88-113">Para obter uma referência para a célula Strikethru pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cbb88-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbb88-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cbb88-114">Cell name:</span></span>  <br/> |<span data-ttu-id="cbb88-115">Char.Strikethru [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cbb88-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cbb88-116">Para obter uma referência para a célula Strikethru pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cbb88-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbb88-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cbb88-117">Section index:</span></span>  <br/> |<span data-ttu-id="cbb88-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="cbb88-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="cbb88-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cbb88-119">Row index:</span></span>  <br/> |<span data-ttu-id="cbb88-120">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cbb88-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cbb88-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cbb88-121">Cell index:</span></span>  <br/> |<span data-ttu-id="cbb88-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="cbb88-122">**visCharacterStrikethru**</span></span> <br/> |
   

