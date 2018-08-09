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
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772028"
---
# <a name="hidetext-cell-miscellaneous-section"></a>Célula HideText (Seção Miscellaneous)

Oculta o texto de uma forma. É possível visualizar o texto, editar as propriedades e aplicar os estilos ao texto no bloco de texto, embora não seja possível visualizar as alterações até que a célula HideText seja redefinida para FALSO (0).
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O texto está oculto e não pode ser impresso.  <br/> |
| FALSO  <br/> | O texto não está oculto.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula HideText pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Célula HideText  <br/> |
   
Para obter uma referência à célula HideText pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visHideText** <br/> |
   

