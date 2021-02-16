---
title: Célula Transparency (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Determina o nível de transparência para uma camada de cor.
ms.openlocfilehash: defe5307e57c433fcf85a4132939d08cb1ddec77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405832"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="a22ba-103">Célula Transparency (Seção Image Properties)</span><span class="sxs-lookup"><span data-stu-id="a22ba-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="a22ba-104">Determina o nível de transparência para uma camada de cor.</span><span class="sxs-lookup"><span data-stu-id="a22ba-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="a22ba-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a22ba-105">**Value**</span></span>|<span data-ttu-id="a22ba-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a22ba-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a22ba-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="a22ba-107">0 - 100</span></span>  <br/> |<span data-ttu-id="a22ba-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="a22ba-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a22ba-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a22ba-110">Remarks</span></span>

<span data-ttu-id="a22ba-p102">Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma camada com cor completamente transparente tenha a mesma aparência de uma camada sem cor na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%. Também é possível definir esse valor usando o controle deslizante na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial**, do grupo **Edição**, clique em **Camadas** e em **Propriedades da Camada**).</span><span class="sxs-lookup"><span data-stu-id="a22ba-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="a22ba-115">Para obter uma referência para a célula Transparency pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a22ba-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22ba-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a22ba-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a22ba-117">Transparência</span><span class="sxs-lookup"><span data-stu-id="a22ba-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="a22ba-118">Para obter uma referência para a célula Transparency pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a22ba-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22ba-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a22ba-119">Section index:</span></span>  <br/> |<span data-ttu-id="a22ba-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a22ba-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a22ba-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="a22ba-121">Row index:</span></span>  <br/> |<span data-ttu-id="a22ba-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="a22ba-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="a22ba-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="a22ba-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a22ba-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="a22ba-124">**visImageTransparency**</span></span> <br/> |
   

