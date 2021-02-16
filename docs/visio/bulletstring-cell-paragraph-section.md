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
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409745"
---
# <a name="bulletstring-cell-paragraph-section"></a>Célula BulletString (Seção Paragraph)

Permite criar um estilo com marcadores personalizados. 
  
## <a name="remarks"></a>Comentários

Insira o estilo como uma cadeia de caracteres (entre aspas). Por exemplo, você poderia inserir a cadeia de caracteres: "ooo".
  
Também é possível definir o valor desta célula clicando com o botão direito do mouse em uma forma, apontando para **Formatar**, clicando em **Texto** e na guia **Marcadores**. 
  
Para obter uma referência para a célula BulletString pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Para.BulletStr[ *i*  ] onde  *i*  = <1>, 2, 3, ...  <br/> |
   
Para obter uma referência para a célula BulletString pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionParagraph** <br/> |
|Índice de linha:  <br/> |**visRowParagraph**  +   *i* onde *i* = 0, 1, 2, ...  <br/> |
|Índice de célula:  <br/> |**visBulletString** <br/> |
   

