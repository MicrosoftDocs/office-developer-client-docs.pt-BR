---
title: Célula InhibitSnap (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Determina se as formas em uma página de primeiro plano são ajustadas a outros objetos na página e a outras formas na página de plano de fundo.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426748"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>Célula InhibitSnap (Seção Page Properties)

Determina se as formas em uma página de primeiro plano são ajustadas a outros objetos na página e a outras formas na página de plano de fundo.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Inibe qualquer ajuste na página, com exceção da régua e da grade.  <br/> |
| FALSE  <br/> | Permite ajustar.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula InhibitSnap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | InhibitSnap  <br/> |
   
Para fazer referência à célula InhibitSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageInhibitSnap** <br/> |
   

