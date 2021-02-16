---
title: Célula UICode (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Determina o código de um campo inserido em versões do Visio anteriores à versão Visio 2000.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422212"
---
# <a name="uicode-cell-text-fields-section"></a>Célula UICode (Seção Text Fields)

Determina o código de um campo inserido em versões do Visio anteriores à versão Visio 2000.
  
## <a name="remarks"></a>Comentários

Esta célula não é exibida na janela ShapeSheet. Utilize essa célula se precisar lidar com questões de capacidade de compatibilidade com versões anteriores, como salvar um desenho do Visio 2000 em um formato de arquivo do Visio 5.0.
  
Para fazer referência à célula UICode pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Fields.UICod[  *i*  ] onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula UICode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTextField** <br/> |
| Índice de linha:  <br/> |**visRowField**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visFieldUICode** <br/> |
   

