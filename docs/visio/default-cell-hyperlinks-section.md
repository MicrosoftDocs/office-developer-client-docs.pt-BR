---
title: Célula Default (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771685"
---
# <a name="default-cell-hyperlinks-section"></a>Célula Default (Seção Hyperlinks)

Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.
  
## <a name="remarks"></a>Comentários

Também é possível definir o hiperlink padrão selecionando uma forma, clicando em **Hiperlink**, na guia **Inserir**, selecionando um hiperlink e clicando em **Padrão**. O hiperlink padrão é exibido em negrito.
  
Para obter uma referência para a célula Default pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *Nome* . Padrão onde Hyperlink. *Name* é o nome da linha  <br/> |
   
Para obter uma referência para a célula Default pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
|Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visHLinkDefault** <br/> |
   

