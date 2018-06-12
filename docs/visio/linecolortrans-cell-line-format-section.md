---
title: Célula LineColorTrans (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Determina o nível de transparência da cor da linha de uma forma.
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772194"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="08073-103">Célula LineColorTrans (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="08073-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="08073-104">Determina o nível de transparência da cor da linha de uma forma.</span><span class="sxs-lookup"><span data-stu-id="08073-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="08073-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="08073-105">**Value**</span></span>|<span data-ttu-id="08073-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08073-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08073-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="08073-107">0 - 100</span></span>  <br/> |<span data-ttu-id="08073-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="08073-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08073-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="08073-110">Remarks</span></span>

<span data-ttu-id="08073-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com uma cor de linha completamente transparente tenha a mesma aparência de uma forma sem linhas na página de desenho, ela irá interagir com os outros objetos da página da mesma forma que se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="08073-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="08073-114">Você também pode definir esse valor usando o controle deslizante na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e, em seguida, clique em **Mais linhas**).</span><span class="sxs-lookup"><span data-stu-id="08073-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="08073-115">Para obter uma referência para a célula LineColorTrans pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="08073-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08073-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="08073-116">Cell name:</span></span>  <br/> |<span data-ttu-id="08073-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="08073-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="08073-118">Para obter uma referência para a célula LineColorTrans pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="08073-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08073-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="08073-119">Section index:</span></span>  <br/> |<span data-ttu-id="08073-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08073-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="08073-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="08073-121">Row index:</span></span>  <br/> |<span data-ttu-id="08073-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="08073-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="08073-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="08073-123">Cell index:</span></span>  <br/> |<span data-ttu-id="08073-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="08073-124">**visLineColorTrans**</span></span> <br/> |
   

