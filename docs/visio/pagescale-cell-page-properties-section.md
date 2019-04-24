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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339449"
---
# <a name="pagescale-cell-page-properties-section"></a>Célula PageScale (Seção Page Properties)

Determina o valor da unidade de página na escala de desenho atual. A escala de desenho da página representa a razão da unidade de página mostrada na célula PageScale em relação à unidade de desenho mostrada na célula DrawingScale.
  
## <a name="remarks"></a>Comentários

Você também pode definir o valor da célula PageScale na guia **Escala de Desenho** na caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta**Configurar Página**). O valor da célula é o primeiro dos dois números nas caixas **Escala Predefinida** ou **Escala Personalizada**, dependendo da definição da escala de desenho selecionada em **Escala de desenho**. Por exemplo, se você selecionar uma escala arquitetônica para o desenho, a escala de desenho para a página é 3/32" = 1'0". O valor da célula PageScale é 0,0938 pol. (ou 3/32") e o valor da célula DrawingScale é 1 pé.
  
Para obter uma referência para a célula PageScale pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PageScale  <br/> |
   
Para obter uma referência para a célula PageScale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPage** <br/> |
|Índice da célula:  <br/> |**visPageScale** <br/> |
   

