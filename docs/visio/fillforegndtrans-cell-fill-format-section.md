---
title: Célula FillForegndTrans (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Determina o nível de transparência para a cor do primeiro plano (preenchimento) do padrão de preenchimento da forma.
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427847"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="38d40-103">Célula FillForegndTrans (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="38d40-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="38d40-104">Determina o nível de transparência para a cor do primeiro plano (preenchimento) do padrão de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="38d40-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="38d40-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="38d40-105">**Value**</span></span>|<span data-ttu-id="38d40-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38d40-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38d40-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="38d40-107">0 - 100</span></span>  <br/> |<span data-ttu-id="38d40-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="38d40-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38d40-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="38d40-110">Remarks</span></span>

<span data-ttu-id="38d40-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com preenchimento completamente transparente tenha a mesma aparência de uma forma sem preenchimento na página de desenho, ela irá interagir com os outros objetos da página da mesma forma que se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="38d40-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="38d40-p103">Você pode também definir o valor utilizando o controle deslizante na caixa de diálogo **Preenchimento** (na guia **Página Inicial**, no grupo **Forma**, clique em **Preenchimento** e em **Opções de preenchimento**). Esse valor controla o valor das transparências de preenchimento do primeiro plano e do plano de fundo. Para definir os valores independentemente, insira-os na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="38d40-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="38d40-117">Para obter uma referência para a célula FillForegndTrans pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="38d40-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38d40-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="38d40-118">Cell name:</span></span>  <br/> |<span data-ttu-id="38d40-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="38d40-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="38d40-120">Para obter uma referência para a célula FillForegndTrans pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="38d40-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38d40-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="38d40-121">Section index:</span></span>  <br/> |<span data-ttu-id="38d40-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="38d40-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="38d40-123">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="38d40-123">Row index:</span></span>  <br/> |<span data-ttu-id="38d40-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="38d40-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="38d40-125">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="38d40-125">Cell index:</span></span>  <br/> |<span data-ttu-id="38d40-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="38d40-126">**visFillForegndTrans**</span></span> <br/> |
   

