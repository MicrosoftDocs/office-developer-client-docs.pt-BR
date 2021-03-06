---
title: Célula LineJumpFactorX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Determina o tamanho dos saltos de linha nos conectores dinâmicos horizontais na página em relação ao valor da célula LineToLineX. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424991"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>Célula LineJumpFactorX (Seção Page Layout)

Determina o tamanho dos saltos de linha nos conectores dinâmicos horizontais na página em relação ao valor da célula LineToLineX. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.
  
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).
  
Para obter uma referência para a célula LineJumpFactorX pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineJumpFactorX  <br/> |
   
Para obter uma referência para a célula LineJumpFactorX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPageLayout** <br/> |
|Índice de célula:  <br/> |**visPLOJumpFactorX** <br/> |
   

