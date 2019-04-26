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
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360274"
---
# <a name="default-cell-hyperlinks-section"></a>Célula Padrão (Seção Hyperlinks)

Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.
  
## <a name="remarks"></a>Comentários

Também é possível definir o hiperlink padrão selecionando uma forma, clicando em **Hiperlink**, na guia **Inserir**, selecionando um hiperlink e clicando em **Padrão**. O hiperlink padrão é exibido em negrito.
  
Para obter uma referência à célula Padrão pelo nome de uma outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *Nome*  .Default           onde Hyperlink. *Name*  é o nome da linha  <br/> |
   
Para obter uma referência à célula Padrão por índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
|Índice de linha:  <br/> |**visRow1stHyperlink** +  *i*           onde *i*  = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visHLinkDefault** <br/> |
   

