---
title: Célula PrintPageOrientation (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Determina se a página será impressa na orientação retrato ou paisagem.
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772607"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Célula PrintPageOrientation (Seção Print Properties)

Determina se a página será impressa na orientação retrato ou paisagem.
  
|**Valor**|**Orientation**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Mesmo que a impressora  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Retrato  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Paisagem  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Coment�rios

Quando você insere novas páginas em um documento, essa configuração padrão é a configuração da página ativa.
  
Para obter uma referência à célula PrintPageOrientation pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PrintPageOrientation  <br/> |
   
Para obter uma referência à célula PrintPageOrientation pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

