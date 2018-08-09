---
title: Célula LineColorTrans (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Determina o nível de transparência da cor da linha de uma forma.
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772194"
---
# <a name="linecolortrans-cell-line-format-section"></a>Célula LineColorTrans (Seção Line Format)

Determina o nível de transparência da cor da linha de uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|
          0 - 100
  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com uma cor de linha completamente transparente tenha a mesma aparência de uma forma sem linhas na página de desenho, ela irá interagir com os outros objetos da página da mesma forma que se a transparência fosse 0%. 
  
Também é possível definir esse valor utilizando o controle deslizante na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Espessura** e clique em **Mais Linhas**).
  
Para obter uma referência para a célula LineColorTrans pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineColorTrans  <br/> |
   
Para obter uma referência para a célula LineColorTrans pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLine** <br/> |
|Índice da célula:  <br/> |**visLineColorTrans** <br/> |
   

