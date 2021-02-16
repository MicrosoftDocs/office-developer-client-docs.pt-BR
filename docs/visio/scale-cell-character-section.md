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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429149"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="f747a-104">Célula Scale (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="f747a-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="f747a-105">Controla a largura da fonte.</span><span class="sxs-lookup"><span data-stu-id="f747a-105">Controls the font width.</span></span> <span data-ttu-id="f747a-106">O valor padrão para esta célula é 100%.</span><span class="sxs-lookup"><span data-stu-id="f747a-106">The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f747a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f747a-107">Remarks</span></span>

<span data-ttu-id="f747a-p103">Defina a porcentagem entre 1% e 99% para diminuir a largura da fonte e entre 101% e 600% para aumentar a largura da fonte.</span><span class="sxs-lookup"><span data-stu-id="f747a-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="f747a-110">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="f747a-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="f747a-111">Para obter uma referência para a célula Scale pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f747a-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f747a-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f747a-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f747a-113">Char.FontScale[ *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f747a-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f747a-114">Para obter uma referência para a célula Scale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f747a-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f747a-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f747a-115">Section index:</span></span>  <br/> |<span data-ttu-id="f747a-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="f747a-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="f747a-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f747a-117">Row index:</span></span>  <br/> |<span data-ttu-id="f747a-118">**visRowCharacter**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f747a-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f747a-119">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="f747a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f747a-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="f747a-120">**visCharacterFontScale**</span></span> <br/> |
   

