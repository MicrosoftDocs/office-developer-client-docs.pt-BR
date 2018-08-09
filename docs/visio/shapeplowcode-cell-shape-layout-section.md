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
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772907"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Célula ShapePlowCode (Seção Shape Layout)

Determina se esta forma de colocação será movida ao soltar outra forma de colocação próxima a esta forma na página de desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Ajustar como especificado na página.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Não ajustar formas.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Ajustar todas as formas.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula para uma determinada forma na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e clique no Guia de **posicionamento** ). 
  
Para definir esse comportamento para *todas* as formas na página de desenho, use a célula PlowCode na seção Page Layout. 
  
Para obter uma referência para a célula ShapePlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePlowCode  <br/> |
   
Para obter uma referência para a célula ShapePlowCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOPlowCode** <br/> |
   

