---
title: Célula BulletString (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permite criar um estilo com marcadores personalizados.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771440"
---
# <a name="bulletstring-cell-paragraph-section"></a>Célula BulletString (Seção Paragraph)

Permite criar um estilo com marcadores personalizados. 
  
## <a name="remarks"></a>Comentários

Insira o estilo como uma cadeia de caracteres (entre aspas). Por exemplo, você poderia inserir a cadeia de caracteres: "ooo".
  
Também é possível definir o valor desta célula clicando com o botão direito do mouse em uma forma, apontando para **Formatar**, clicando em **Texto** e na guia **Marcadores**. 
  
Para obter uma referência para a célula BulletString pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Para.BulletStr [ *i* ] onde *i* = < 1 >, 2, 3,...  <br/> |
   
Para obter uma referência para a célula BulletString pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionParagraph** <br/> |
|Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visBulletString** <br/> |
   

