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
description: Determina o estilo com marcadores.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771433"
---
# <a name="bullet-cell-paragraph-section"></a>Célula Bullet (Seção Paragraph)

Determina o estilo com marcadores.
  
|**Valor**|**Estilo com marcadores**|
|:-----|:-----|
|0  <br/> |Nenhum  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
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
|Nome da célula:  <br/> |Para.Bullet [ *i* ] onde *i* = < 1 >, 2, 3,...  <br/> |
   
Para obter uma referência para a célula Bullet pelo índice, a partir de um programa, use a propriedade  **CellsSRC**com os seguintes argumentos: 
  

