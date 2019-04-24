---
title: Célula HideText (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Oculta o texto de uma forma. É possível visualizar o texto, editar as propriedades e aplicar os estilos ao texto no bloco de texto, embora não seja possível visualizar as alterações até que a célula HideText seja redefinida para FALSO (0).
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329957"
---
# <a name="hidetext-cell-miscellaneous-section"></a>Célula HideText (Seção Miscellaneous)

Oculta o texto de uma forma. É possível visualizar o texto, editar as propriedades e aplicar os estilos ao texto no bloco de texto, embora não seja possível visualizar as alterações até que a célula HideText seja redefinida para FALSO (0).
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | O texto está oculto e não pode ser impresso.  <br/> |
| FALSE  <br/> | O texto não está oculto.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula HideText pelo nome, a partir de outra fórmula ou programa que usa **** a propriedade Cells, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | HideText  <br/> |
   
Para obter uma referência para a célula HideText pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visHideText** <br/> |
   

