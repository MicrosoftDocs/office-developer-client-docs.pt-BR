---
title: Célula TextBkgndTrans (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Determina o nível de transparência para a cor do plano de fundo do bloco de texto da forma.
ms.openlocfilehash: f4c4dc7700c553bd4c9bee337220e357c4c5538a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408688"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="36d31-103">Célula TextBkgndTrans (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="36d31-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="36d31-104">Determina o nível de transparência para a cor do plano de fundo do bloco de texto da forma.</span><span class="sxs-lookup"><span data-stu-id="36d31-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="36d31-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="36d31-105">**Value**</span></span>|<span data-ttu-id="36d31-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36d31-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36d31-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="36d31-107">0 - 100</span></span>  <br/> |<span data-ttu-id="36d31-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="36d31-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36d31-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="36d31-110">Remarks</span></span>

<span data-ttu-id="36d31-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com um plano de fundo de texto completamente transparente tenha a mesma aparência de uma forma sem plano de fundo de texto na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="36d31-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="36d31-114">Você pode também definir o valor utilizando o controle deslizante na guia **Fonte** da caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="36d31-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="36d31-115">Para obter uma referência para a célula TextBkgndTrans pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="36d31-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36d31-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="36d31-116">Cell name:</span></span>  <br/> |<span data-ttu-id="36d31-117">TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="36d31-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="36d31-118">Para obter uma referência para a célula TextBkgndTrans pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="36d31-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36d31-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="36d31-119">Section index:</span></span>  <br/> |<span data-ttu-id="36d31-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36d31-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="36d31-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="36d31-121">Row index:</span></span>  <br/> |<span data-ttu-id="36d31-122">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="36d31-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="36d31-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="36d31-123">Cell index:</span></span>  <br/> |<span data-ttu-id="36d31-124">**visTxtBlkBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="36d31-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

