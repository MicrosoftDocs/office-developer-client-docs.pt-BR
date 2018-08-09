---
title: Célula NonPrinting (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Alterna entre imprimir ou não a forma selecionada.
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772414"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Célula NonPrinting (Seção Miscellaneous)

Alterna entre imprimir ou não a forma selecionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Impressão desativada, mas a forma será exibida na janela de desenho.  <br/> |
| FALSO  <br/> | Impressão ativada.  <br/> |
   
## <a name="remarks"></a>Comentários

É possível imprimir um guia selecionando-o e definindo o valor de sua célula NonPrinting para FALSO.
  
Para fazer referência à célula NonPrinting pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | NonPrinting  <br/> |
   
Para fazer referência à célula NonPrinting pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visNonPrinting** <br/> |
   

