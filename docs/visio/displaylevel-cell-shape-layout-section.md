---
title: Célula DisplayLevel (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Determina a faixa de níveis de exibição (o intervalo relativo do agrupamento da ordem Z) para a forma.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408142"
---
# <a name="displaylevel-cell-shape-layout-section"></a>Célula DisplayLevel (Seção Shape Layout)

Determina a faixa de níveis de exibição (o intervalo relativo do agrupamento da ordem Z) para a forma.
  
## <a name="remarks"></a>Comentários

Ordem Z é a ordem de exibição das formas na página de desenho. Uma forma posicionada mais alto nessa ordem aparecerá na frente de uma forma que esteja mais baixo quando uma delas sobrepuser a outra. 
  
O nível de exibição divide as formas em agrupamentos (também conhecidos como faixas). Todas as formas em uma determinada faixa têm uma ordem Z mais alta que as existentes em uma faixa mais baixa. Por padrão, o nível de exibição da maioria das formas é zero (0).
  
O intervalo de níveis de exibição varia de -32.767 a +32.767. Formas com o mesmo nível de exibição são combinadas em uma única faixa, dentro da qual também são classificadas em relação umas às outras pela ordem Z.
  
Você pode alterar a ordem Z das formas dentro de uma banda usando os comandos **Bring Forward**, **Send Backward**, Bring to **Front** e Send **to Back**. Se esses comandos moverem uma forma para fora da faixa determinada, o Microsoft Visio exibirá o valor reservado -32.768 na célula DisplayLevel da forma, a menos que a célula esteja protegida. Nesse caso, a forma não poderá ser movida para outra faixa e o Visio exibirá o aviso "A proteção da forma e/ou as propriedades da camada impedem a execução completa deste comando". 
  
Para obter uma referência à célula DisplayLevel pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |DisplayLevel  <br/> |
   
Para obter uma referência à célula DisplayLevel pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLODisplayLevel** <br/> |
   

