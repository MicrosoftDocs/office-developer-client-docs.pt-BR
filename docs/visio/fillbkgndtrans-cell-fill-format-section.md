---
title: Célula FillBkgndTrans (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
localization_priority: Normal
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: Determina o nível de transparência para a cor do plano de fundo (preenchimento) do padrão de preenchimento da forma.
ms.openlocfilehash: c8dcec8cc0bdb87700bb85754298ec4755bae7d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771870"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a><span data-ttu-id="4cc38-103">Célula FillBkgndTrans (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="4cc38-103">FillBkgndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="4cc38-104">Determina o nível de transparência para a cor do plano de fundo (preenchimento) do padrão de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="4cc38-104">Determines the transparency level for the background (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="4cc38-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4cc38-105">**Value**</span></span>|<span data-ttu-id="4cc38-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4cc38-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cc38-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="4cc38-107">0 - 100</span></span>  <br/> |<span data-ttu-id="4cc38-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="4cc38-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cc38-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cc38-110">Remarks</span></span>

<span data-ttu-id="4cc38-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com preenchimento completamente transparente tenha a mesma aparência de uma forma sem preenchimento na página de desenho, ela irá interagir com os outros objetos da página da mesma forma que se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="4cc38-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="4cc38-114">Você também pode definir o valor utilizando o controle deslizante na caixa de diálogo **preenchimento** (na guia **página inicial** , no grupo **forma** , clique em **preenchimento**e, em seguida, clique em **Opções de preenchimento**).</span><span class="sxs-lookup"><span data-stu-id="4cc38-114">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span> <span data-ttu-id="4cc38-115">Esse valor controla o valor das transparências de preenchimento de primeiro plano e plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="4cc38-115">This value controls the value of both the background and foreground fill transparencies.</span></span> <span data-ttu-id="4cc38-116">Para definir esses valores de forma independente, você deverá inseri-los na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4cc38-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="4cc38-117">Para obter uma referência para a célula FillBkgndTrans pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="4cc38-117">To get a reference to the FillBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cc38-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4cc38-118">Cell name:</span></span>  <br/> |<span data-ttu-id="4cc38-119">FillBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="4cc38-119">FillBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="4cc38-120">Para obter uma referência para a célula FillBkgndTrans pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4cc38-120">To get a reference to the FillBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cc38-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4cc38-121">Section index:</span></span>  <br/> |<span data-ttu-id="4cc38-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4cc38-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4cc38-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4cc38-123">Row index:</span></span>  <br/> |<span data-ttu-id="4cc38-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="4cc38-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="4cc38-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4cc38-125">Cell index:</span></span>  <br/> |<span data-ttu-id="4cc38-126">**visFillBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="4cc38-126">**visFillBkgndTrans**</span></span> <br/> |
   

