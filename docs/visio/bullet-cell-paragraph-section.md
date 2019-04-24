---
title: Célula Bullet (seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Determina o estilo de marcador.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338161"
---
# <a name="bullet-cell-paragraph-section"></a>Célula Bullet (seção Paragraph)

Determina o estilo de marcador.
  
|**Valor**|**Estilo de marcador**|
|:-----|:-----|
|,0  <br/> |Nenhum  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|duas  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3D  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|quatro  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|0,5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|178  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionParagraph** <br/> |
|Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor desta célula clicando com o botão direito do mouse em uma forma, apontando para **Formatar**, clicando em **Texto** e na guia **Marcadores**. 
  
Para obter uma referência para a célula Bullet pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Para. Bullet [ *i* ] onde *i* = <1>, 2, 3,...  <br/> |
   
Para obter uma referência para a célula Bullet pelo índice, a partir de um programa, use a propriedade  **CellsSRC**com os seguintes argumentos: 
  

