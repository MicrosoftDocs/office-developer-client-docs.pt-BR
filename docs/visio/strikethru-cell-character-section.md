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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412426"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="6d628-103">Célula Strikethru (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="6d628-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="6d628-104">Determina se o texto está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="6d628-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="6d628-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d628-105">**Value**</span></span>|<span data-ttu-id="6d628-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d628-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d628-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="6d628-107">TRUE</span></span>  <br/> |<span data-ttu-id="6d628-108">O texto está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="6d628-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="6d628-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6d628-109">FALSE</span></span>  <br/> |<span data-ttu-id="6d628-110">O texto não está formatado como tachado.</span><span class="sxs-lookup"><span data-stu-id="6d628-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d628-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d628-111">Remarks</span></span>

<span data-ttu-id="6d628-112">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="6d628-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="6d628-113">Para obter uma referência para a célula Strikethru pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6d628-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d628-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6d628-114">Cell name:</span></span>  <br/> |<span data-ttu-id="6d628-115">Char.Strikethru[ *i*  ] onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6d628-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6d628-116">Para obter uma referência para a célula Strikethru pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6d628-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d628-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6d628-117">Section index:</span></span>  <br/> |<span data-ttu-id="6d628-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="6d628-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="6d628-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6d628-119">Row index:</span></span>  <br/> |<span data-ttu-id="6d628-120">**visRowCharacter**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d628-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6d628-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="6d628-121">Cell index:</span></span>  <br/> |<span data-ttu-id="6d628-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="6d628-122">**visCharacterStrikethru**</span></span> <br/> |
   

