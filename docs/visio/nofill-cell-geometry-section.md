---
title: Célula NoFill (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indica se um caminho pode ser preenchido.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415016"
---
# <a name="nofill-cell-geometry-section"></a>Célula NoFill (Seção Geometry)

Indica se um caminho pode ser preenchido.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O caminho não é preenchido mesmo se outros caminhos da forma forem preenchidos.  <br/> |
| FALSE  <br/> | O preenchimento da forma é aplicado ao caminho, mesmo se não estiver fechado.  <br/> |
   
## <a name="remarks"></a>Comentários

Se você definir o padrão de preenchimento de uma forma para nenhum (0), nenhum de seus caminhos serão preenchidos. Esta célula é utilizada para desativar seletivamente o preenchimento do caminho em uma forma.
  
Para fazer referência à célula NoFill pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry *i* . NoFill onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula NoFill pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowComponent** <br/> |
| Índice da célula:  <br/> |**visCompNoFill** <br/> |
   

