---
title: Célula LineColor (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Determina a cor da linha da forma.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416934"
---
# <a name="linecolor-cell-line-format-section"></a>Célula LineColor (Seção Line Format)

Determina a cor da linha da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor da linha, insira um número de 0 a 23, que serve como um índice para uma coleção de cores de linha. É possível visualizar a coleção de cores de linha na caixa de diálogo **Linha** (na guia **Página Inicial** no grupo **Forma**, clique em **Linha**, aponte para **Espessura** e clique em **Mais Linhas**). Você também pode definir o valor da célula LineColor na caixa de diálogo **Linha**). 
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é sua cor RGB e RGB ( *r, g, b*), e não um número, serão mostrados na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24. 
  
É possível definir a transparência da cor de linha na célula LineColorTrans.
  
Para obter uma referência para a célula LineColor pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineColor  <br/> |
   
Para obter uma referência para a célula LineColor pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLine** <br/> |
|Índice de célula:  <br/> |**visLineColor** <br/> |
   

