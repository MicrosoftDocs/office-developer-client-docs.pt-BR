---
title: Linha Controls (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
localization_priority: Normal
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: Contém as células que definem os x e y-coordenadas e o comportamento de cada alça de controle definida para uma forma. Uma forma conterá uma linha Controls para cada alça de controle.
ms.openlocfilehash: ed1d57fce6d413b9eb7f5d119264bc2bfa968222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771609"
---
# <a name="controls-row-controls-section"></a>Linha Controls (Seção Controls)

Contém as células que definem os *x* e *y* -coordenadas e o comportamento de cada alça de controle definida para uma forma. Uma forma conterá uma linha Controls para cada alça de controle. 
  
As linhas Controls são denominadas Controls. *nome* e contém as células a seguir. Para obter mais detalhes, consulte os tópicos de célula específica. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Representa o *x* -coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Representa o *y* -coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Representa o *x* -coordenadas para o ponto de ancoragem de uma alça de controle em coordenadas locais.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Representa o *y* -coordenadas para o ponto de ancoragem de uma alça de controle em coordenadas locais.  <br/> |
|[X comportamento](x-behavior-cell-controls-section.md) <br/> |Controla o tipo de comportamento no *x* -coordenadas da alça de controle irá exibir depois da alça ser movida.  <br/> |
|[Comportamento de Y](y-behavior-cell-controls-section.md) <br/> |Controla o tipo de comportamento *y* -coordenadas da alça de controle irá exibir depois da alça ser movida.  <br/> |
|[CAN Glue](can-glue-cell-controls-section.md) <br/> |Determina se é possível associar uma alça de controle a outras formas.  <br/> |
|[Dica](tip-cell-controls-section.md) <br/> |Representa uma sequência de texto descritiva exibida como uma Dica de Ferramenta quando o usuário pausa o ponteiro sobre a alça de controle de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

 Você pode adicionar quantos controles.  linhas de *nome* conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar as alças de controle a uma seção Controls existente, do mouse em uma linha e clique em **Inserir linha** no menu de atalho. 
  
Você pode fazer referência a essas células pelo nome da linha, exibido em uma janela ShapeSheet em texto vermelho. Para atribuir nomes significativos aos controles. linhas de *nome* , clique na linha e digite *personalizado* , por exemplo, para criar o nome da linha Custom. Você pode fazer referência à célula X usando Controls.Custom.X. 
  
O nome de linha inserido deve ser único na seção.
  

