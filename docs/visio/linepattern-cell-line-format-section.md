---
title: Célula LinePattern (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Determina o padrão de linha de uma forma. O valor inserido na célula LinePattern é um número que serve de índice para uma coleção de padrões de linha.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772200"
---
# <a name="linepattern-cell-line-format-section"></a>Célula LinePattern (Seção Line Format)

Determina o padrão de linha de uma forma. O valor inserido na célula LinePattern é um número que serve de índice para uma coleção de padrões de linha.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Sem padrão de linha  <br/> |
|1  <br/> |Sólido  <br/> |
|2 - 23  <br/> |Padrões de linha variados  <br/> |
   
## <a name="remarks"></a>Comentários

É possível visualizar a coleção de padrões de linha na caixa de diálogo **Linha** (na guia **Página Inicial** no grupo **Forma**, clique em **Linha**, aponte para **Traços** e clique em **Mais Linhas**).
  
Para especificar um padrão de linha personalizado, utilize a função USE desta célula.
  
Para obter uma referência para a célula LinePattern pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LinePattern  <br/> |
   
Para obter uma referência para a célula LinePattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLine** <br/> |
|Índice da célula:  <br/> |**visLinePattern** <br/> |
   

