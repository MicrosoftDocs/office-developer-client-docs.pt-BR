---
title: Célula PageScale (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Determina o valor da unidade de página na escala de desenho atual. A escala de desenho da página representa a razão da unidade de página mostrada na célula PageScale em relação à unidade de desenho mostrada na célula DrawingScale.
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405531"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="6638c-104">Célula PageScale (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="6638c-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="6638c-p102">Determina o valor da unidade de página na escala de desenho atual. A escala de desenho da página representa a razão da unidade de página mostrada na célula PageScale em relação à unidade de desenho mostrada na célula DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="6638c-p102">Determines the value of the page unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6638c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6638c-107">Remarks</span></span>

<span data-ttu-id="6638c-p103">Você também pode definir o valor da célula PageScale na guia **Escala de Desenho** na caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta **Configurar Página**). O valor da célula é o primeiro dos dois números nas caixas **Escala Predefinida** ou **Escala Personalizada**, dependendo da definição da escala de desenho selecionada em **Escala de desenho**. Por exemplo, se você selecionar uma escala arquitetônica para o desenho, a escala de desenho para a página é 3/32" = 1'0". O valor da célula PageScale é 0,0938 pol. (ou 3/32") e o valor da célula DrawingScale é 1 pé.</span><span class="sxs-lookup"><span data-stu-id="6638c-p103">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**. For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0". The value in the PageScale cell is 0.0938 in. (or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="6638c-113">Para obter uma referência para a célula PageScale pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6638c-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6638c-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6638c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="6638c-115">PageScale</span><span class="sxs-lookup"><span data-stu-id="6638c-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="6638c-116">Para obter uma referência para a célula PageScale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6638c-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6638c-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6638c-117">Section index:</span></span>  <br/> |<span data-ttu-id="6638c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6638c-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6638c-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6638c-119">Row index:</span></span>  <br/> |<span data-ttu-id="6638c-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="6638c-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="6638c-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="6638c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="6638c-122">**visPageScale**</span><span class="sxs-lookup"><span data-stu-id="6638c-122">**visPageScale**</span></span> <br/> |
   

