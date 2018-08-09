---
title: Célula DrawingScale (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Representa o valor da unidade de desenho na escala de desenho atual. A escala de desenho da página representa a razão da unidade de página mostrada na célula PageScale em relação à unidade de desenho mostrada na célula DrawingScale.
ms.openlocfilehash: cdd3222f5e56c34ac8947c9ef5a653cfe19fbd0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771756"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="81066-104">Célula DrawingScale (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="81066-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="81066-p102">Representa o valor da unidade de desenho na escala de desenho atual. A escala de desenho da página representa a razão da unidade de página mostrada na célula PageScale em relação à unidade de desenho mostrada na célula DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="81066-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="81066-p103">É possível configurar a célula DrawingScale para alterar as unidades das réguas de uma página de um programa. Este é um exemplo de como alterar as unidades de medida de um programa de polegadas para centímetros. Nesse caso, o método **ConvertResult** é utilizado para manter a mesma distância, mas com unidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="81066-p103">You can set the DrawingScale cell to change the units of a page's rulers from a program. Here is an example of changing the measurement units from inches to centimeters from a program. In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="81066-110">Você pode determinar o sistema de medida em um desenho examinando a propriedade **unidades** da célula DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="81066-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="81066-111">Depois de executar a macro acima a seguinte instrução executada nos Immediate Editor do Visual Basic janela retornará *True* .</span><span class="sxs-lookup"><span data-stu-id="81066-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="81066-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="81066-112">Remarks</span></span>

<span data-ttu-id="81066-113">Esta célula corresponde às configurações da caixa de diálogo **Configurar Página** (clique na seta **Configurar Página** na guia **Página Inicial** ).</span><span class="sxs-lookup"><span data-stu-id="81066-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="81066-p105">As unidades da fórmula na célula DrawingScale determinam as unidades de medida utilizadas pelas réguas na janela de desenho. Se você não quiser alterar também a dimensão do desenho, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="81066-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="81066-116">Mantenha a mesma distância indicada na célula DrawingScale, mas com unidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="81066-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="81066-117">Altere a distância indicada na célula PageScale pelo mesmo fator utilizado em DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="81066-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="81066-118">Para obter uma referência para a célula Color pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="81066-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81066-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="81066-119">Cell name:</span></span>  <br/> |<span data-ttu-id="81066-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="81066-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="81066-121">Para obter uma referência para a célula DrawingScale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="81066-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81066-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="81066-122">Section index:</span></span>  <br/> |<span data-ttu-id="81066-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81066-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="81066-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="81066-124">Row index:</span></span>  <br/> |<span data-ttu-id="81066-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="81066-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="81066-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="81066-126">Cell index:</span></span>  <br/> |<span data-ttu-id="81066-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="81066-127">**visPageDrawingScale**</span></span> <br/> |
   

