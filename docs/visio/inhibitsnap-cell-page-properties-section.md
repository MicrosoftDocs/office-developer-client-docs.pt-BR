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
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772077"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>Célula InhibitSnap (Seção Page Properties)

Determina se as formas em uma página de primeiro plano são ajustadas a outros objetos na página e a outras formas na página de plano de fundo.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Inibe qualquer ajuste na página, com exceção da régua e da grade.  <br/> |
| FALSO  <br/> | Permite ajustar.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula InhibitSnap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | InhibitSnap  <br/> |
   
Para obter uma referência à célula InhibitSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageInhibitSnap** <br/> |
   

