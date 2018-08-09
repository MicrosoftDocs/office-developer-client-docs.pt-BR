---
title: Célula Transparency (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Determina o nível de transparência de um intervalo na cor de texto de uma forma.
ms.openlocfilehash: 5914a061b1bba2173b338544b05abda8780ff164
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773164"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="95af9-103">Célula Transparency (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="95af9-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="95af9-104">Determina o nível de transparência de um intervalo na cor de texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="95af9-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="95af9-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="95af9-105">**Value**</span></span>|<span data-ttu-id="95af9-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95af9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95af9-107">
          0 - 100
</span><span class="sxs-lookup"><span data-stu-id="95af9-107">0 - 100</span></span>  <br/> |<span data-ttu-id="95af9-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="95af9-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95af9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="95af9-110">Remarks</span></span>

<span data-ttu-id="95af9-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com texto completamente transparente tenha a mesma aparência de uma forma sem texto na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="95af9-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="95af9-114">Você também pode definir esse valor usando o controle deslizante na guia **fonte** na caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ).</span><span class="sxs-lookup"><span data-stu-id="95af9-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="95af9-p103">Se a seção Caracteres contiver diversas linhas, a célula Transparency conterá informações de formatação aplicada a um subintervalo de texto de uma forma. Caso contrário, ela conterá informações de formatação para todo o texto da forma.</span><span class="sxs-lookup"><span data-stu-id="95af9-p103">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="95af9-117">Para obter uma referência para a célula Transparency pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="95af9-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95af9-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="95af9-118">Cell name:</span></span>  <br/> |<span data-ttu-id="95af9-119">Char.ColorTrans [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="95af9-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95af9-120">Para obter uma referência para a célula Transparency pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="95af9-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95af9-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="95af9-121">Section index:</span></span>  <br/> |<span data-ttu-id="95af9-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="95af9-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="95af9-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="95af9-123">Row index:</span></span>  <br/> |<span data-ttu-id="95af9-124">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95af9-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="95af9-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="95af9-125">Cell index:</span></span>  <br/> |<span data-ttu-id="95af9-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="95af9-126">**visCharacterColorTrans**</span></span> <br/> |
   
