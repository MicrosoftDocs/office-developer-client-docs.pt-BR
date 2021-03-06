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
description: Contém células que definem as coordenadas x e y e o comportamento de cada alça de controle definida para uma forma. Uma forma conterá uma linha Controls para cada alça de controle.
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438187"
---
# <a name="controls-row-controls-section"></a>Linha Controls (Seção Controls)

Contém células que definem as  *coordenadas x*  e  *y*  e o comportamento de cada alça de controle definida para uma forma. Uma forma conterá uma linha Controls para cada alça de controle. 
  
As linhas Controls são denominadas Controls. *e*  contenha as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Representa a  *coordenada x*  que indica o local da alça de controle de uma forma em coordenadas locais.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Representa a  *coordenada y*  que indica o local da alça de controle de uma forma em coordenadas locais.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Representa a  *coordenada x*  do ponto de ancoragem de uma alça de controle em coordenadas locais.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Representa a  *coordenada y*  do ponto de ancoragem de uma alça de controle em coordenadas locais.  <br/> |
|[X Behavior](x-behavior-cell-controls-section.md) <br/> |Controla o tipo de comportamento que a coordenada  *x*  da alça de controle exibirá depois que a alça for movida.  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |Controla o tipo de comportamento que a coordenada  *y*  da alça de controle exibirá depois que a alça for movida.  <br/> |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |Determina se é possível associar uma alça de controle a outras formas.  <br/> |
|[Dica](tip-cell-controls-section.md) <br/> |Representa uma sequência de texto descritiva exibida como uma Dica de Ferramenta quando o usuário pausa o ponteiro sobre a alça de controle de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

 É possível adicionar tantas linhas Controls.  *name* quantas forem necessárias, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar alças de controle a uma seção Controls existente, clique com o botão direito do mouse em uma linha e clique em **Inserir Linha** no menu de atalho. 
  
É possível fazer referência a essas células pelo nome da linha, exibido na janela ShapeSheet em texto vermelho. Para atribuir nomes significativos às linhas Controls. *name*  rows, click the row and then type  *Custom*  , for example, to create the row name Controls.Custom. Você pode fazer referência à célula X usando Controls.Custom.X. 
  
O nome de linha inserido deve ser único na seção.
  

