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
ms.openlocfilehash: f9b09d67bc8d9ae851e86eaaa2ce1d36a92b2da2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771871"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="d9dac-103">Célula FillForegndTrans (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="d9dac-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="d9dac-104">Determina o nível de transparência para a cor do primeiro plano (preenchimento) do padrão de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="d9dac-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="d9dac-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d9dac-105">**Value**</span></span>|<span data-ttu-id="d9dac-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d9dac-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9dac-107">
          0 - 100
</span><span class="sxs-lookup"><span data-stu-id="d9dac-107">0 - 100</span></span>  <br/> |<span data-ttu-id="d9dac-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="d9dac-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9dac-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9dac-110">Remarks</span></span>

<span data-ttu-id="d9dac-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com preenchimento completamente transparente tenha a mesma aparência de uma forma sem preenchimento na página de desenho, ela irá interagir com os outros objetos da página da mesma forma que se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="d9dac-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="d9dac-p103">Você pode também definir o valor utilizando o controle deslizante na caixa de diálogo **Preenchimento** (na guia **Página Inicial**, no grupo **Forma**, clique em **Preenchimento** e em **Opções de preenchimento**). Esse valor controla o valor das transparências de preenchimento do primeiro plano e do plano de fundo. Para definir os valores independentemente, insira-os na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d9dac-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="d9dac-117">Para obter uma referência para a célula FillForegndTrans pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d9dac-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9dac-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d9dac-118">Cell name:</span></span>  <br/> |<span data-ttu-id="d9dac-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="d9dac-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="d9dac-120">Para obter uma referência para a célula FillForegndTrans pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d9dac-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9dac-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d9dac-121">Section index:</span></span>  <br/> |<span data-ttu-id="d9dac-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d9dac-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d9dac-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d9dac-123">Row index:</span></span>  <br/> |<span data-ttu-id="d9dac-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d9dac-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="d9dac-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d9dac-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d9dac-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="d9dac-126">**visFillForegndTrans**</span></span> <br/> |
   

