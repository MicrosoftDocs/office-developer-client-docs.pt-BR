---
title: Célula ShapePlowCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Determina se esta forma de colocação será movida ao soltar outra forma de colocação próxima a esta forma na página de desenho.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423892"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Célula ShapePlowCode (Seção Shape Layout)

Determina se esta forma de colocação será movida ao soltar outra forma de colocação próxima a esta forma na página de desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Ajustar como especificado na página.  <br/> |**visSLOPlowDefault** <br/> |
|1   <br/> |Não ajustar formas.  <br/> |**visSLOPlowNever** <br/> |
|2   <br/> |Ajustar todas as formas.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula para uma forma específica na guia Posicionamento [](run-in-developer-mode-display-the-developer-tab.md) na caixa de diálogo Comportamento (com uma forma  selecionada, na guia Desenvolvedor, no grupo **Design** da Forma, clique em Comportamento e na guia Posicionamento).    
  
Para definir esse comportamento para  *todas as*  formas na página de desenho, use a célula PlowCode na seção Page Layout. 
  
Para obter uma referência para a célula ShapePlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePlowCode  <br/> |
   
Para obter uma referência para a célula ShapePlowCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLOPlowCode** <br/> |
   

