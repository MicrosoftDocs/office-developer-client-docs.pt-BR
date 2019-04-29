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
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437256"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Célula NonPrinting (Seção Miscellaneous)

Alterna entre imprimir ou não a forma selecionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Impressão desativada, mas a forma será exibida na janela de desenho.  <br/> |
| FALSE  <br/> | Impressão ativada.  <br/> |
   
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
| Índice de linha:  <br/> |**visRowMisc** <br/> |
| Índice de célula:  <br/> |**visNonPrinting** <br/> |
   

