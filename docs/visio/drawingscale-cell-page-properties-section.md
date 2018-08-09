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
# <a name="drawingscale-cell-page-properties-section"></a>Célula DrawingScale (Seção Page Properties)

Representa o valor da unidade de desenho na escala de desenho atual. A escala de desenho da página representa a razão da unidade de página mostrada na célula PageScale em relação à unidade de desenho mostrada na célula DrawingScale.
  
É possível configurar a célula DrawingScale para alterar as unidades das réguas de uma página de um programa. Este é um exemplo de como alterar as unidades de medida de um programa de polegadas para centímetros. Nesse caso, o método **ConvertResult** é utilizado para manter a mesma distância, mas com unidades diferentes. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Você pode determinar o sistema de medida em um desenho examinando a propriedade **unidades** da célula DrawingScale. Depois de executar a macro acima a seguinte instrução executada nos Immediate Editor do Visual Basic janela retornará *True* . 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Comentários

Esta célula corresponde às configurações da caixa de diálogo **Configurar Página** (clique na seta **Configurar Página** na guia **Página Inicial** ). 
  
As unidades da fórmula na célula DrawingScale determinam as unidades de medida utilizadas pelas réguas na janela de desenho. Se você não quiser alterar também a dimensão do desenho, siga um destes procedimentos:
  
- Mantenha a mesma distância indicada na célula DrawingScale, mas com unidades diferentes.
    
- Altere a distância indicada na célula PageScale pelo mesmo fator utilizado em DrawingScale.
    
Para obter uma referência para a célula Color pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |DrawingScale  <br/> |
   
Para obter uma referência para a célula DrawingScale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPage** <br/> |
|Índice da célula:  <br/> |**visPageDrawingScale** <br/> |
   

