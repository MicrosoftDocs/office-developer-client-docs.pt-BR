---
title: Célula LineJumpFactorY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Determina o tamanho dos saltos de linha nos conectores dinâmicos verticais na página em relação ao valor da célula LineToLineY. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.
ms.openlocfilehash: deba4c27585644604e7bac1dbfe284bc3977835e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772213"
---
# <a name="linejumpfactory-cell-page-layout-section"></a>Célula LineJumpFactorY (Seção Page Layout)

Determina o tamanho dos saltos de linha nos conectores dinâmicos verticais na página em relação ao valor da célula LineToLineY. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.
  
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).
  
Para obter uma referência para a célula LineJumpFactorY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineJumpFactorY  <br/> |
   
Para obter uma referência para a célula LineJumpFactorY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOJumpFactorY** <br/> |
   

