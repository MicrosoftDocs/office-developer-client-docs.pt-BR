---
title: Célula Scale (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Controla a largura da fonte. O valor padrão para esta célula é 100%.
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341626"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="5099e-104">Célula Scale (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="5099e-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="5099e-105">Controla a largura da fonte.</span><span class="sxs-lookup"><span data-stu-id="5099e-105">Controls the font width.</span></span> <span data-ttu-id="5099e-106">O valor padrão para esta célula é 100%.</span><span class="sxs-lookup"><span data-stu-id="5099e-106">The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5099e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5099e-107">Remarks</span></span>

<span data-ttu-id="5099e-p103">Defina a porcentagem entre 1% e 99% para diminuir a largura da fonte e entre 101% e 600% para aumentar a largura da fonte.</span><span class="sxs-lookup"><span data-stu-id="5099e-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="5099e-110">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="5099e-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="5099e-111">Para obter uma referência para a célula Scale pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="5099e-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5099e-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5099e-112">Cell name:</span></span>  <br/> |<span data-ttu-id="5099e-113">Char. FontScale [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5099e-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5099e-114">Para obter uma referência para a célula Scale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5099e-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5099e-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5099e-115">Section index:</span></span>  <br/> |<span data-ttu-id="5099e-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="5099e-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="5099e-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5099e-117">Row index:</span></span>  <br/> |<span data-ttu-id="5099e-118">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5099e-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5099e-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5099e-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5099e-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="5099e-120">**visCharacterFontScale**</span></span> <br/> |
   

