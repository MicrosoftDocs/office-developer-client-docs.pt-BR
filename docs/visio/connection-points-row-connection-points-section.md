---
title: Linha Connection Points (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3005
localization_priority: Normal
ms.assetid: eaac62a5-f516-9b81-587a-8e0e02de59ee
description: Contém as coordenadas x e y, direção horizontal e vertical e o tipo de um ponto de conexão único em uma forma. As coordenadas dos pontos de conexão são medidas na origem da forma. Uma forma contém uma linha Connection Points para cada ponto de conexão.
ms.openlocfilehash: 301ea4fb446d9acafd4b59af388c3e7b2d419e20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415506"
---
# <a name="connection-points-row-connection-points-section"></a>Linha Connection Points (Seção Connection Points)

Contém as coordenadas *x* e *y*, direção horizontal e vertical e o tipo de um ponto de conexão único em uma forma. As coordenadas dos pontos de conexão são medidas na origem da forma. Uma forma contém uma linha Connection Points para cada ponto de conexão. 
  
Se as linhas dos Pontos de Conexão são nomeadas, esses nomes aparecerão como Connections. *name* na janela ShapeSheet. As linhas Connection Points contêm as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |A coordenada *x* de um ponto de conexão em coordenadas locais.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |A coordenada *y* de um ponto de conexão em coordenadas locais.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |O componente *x* do vetor de alinhamento necessário de um ponto de conexão correspondente. Ela também é utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |O componente *y* do vetor de alinhamento necessário de um ponto de conexão correspondente. Ela também é utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |O tipo de ponto de conexão (0 = para dentro; 1 = para fora; 2 = para dentro + para fora).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas. Para acessar essa célula, clique com o botão direito do mouse em uma linha e clique em **Alterar Tipo de Linha **no menu de atalho.<br/> |
   
## <a name="remarks"></a>Comentários

Células em Connections. *name* são rotuladas DirX/A, DirY/B e Type/C porque essas linhas podem ser estendidas ou não-estendidas. 
  
A maioria dos pontos de conexão (todos os pontos de conexão criados pela interface do usuário) é não-estendida e contém células DirX, DirY e Type. Seus tipos de linha são **visTagCnnctPt** ou **visTagCnnctNamed**.
  
Em linhas não-estendidas, as células DirX e DirY juntas definem um vetor de direção que influencia a rotação de formas envolvidas em conexões usando o ponto de conexão. Se ambas forem zero, o ponto não terá direção. Os pontos de conexão são do seguinte tipo:
  
- Para dentro (0), o que significa que as formas são coladas a ele. É o padrão.
    
- Para fora (1), o que significa que esses pontos de conexão serão colados a pontos de conexão para dentro.
    
- Tanto para dentro como para fora (2), caso em que a direção é para dentro, sendo revertida se usada como uma conexão para fora.
    
As linhas estendidas contêm células A, B, C e D e se comportam como as linhas não-estendidas sem direção do tipo Para dentro. Normalmente, as linhas estendidas não são utilizadas, mas você pode precisar usá-las para associar os dados a um ponto de conexão nas células A, B, C e D. Seu tipo de linha é **visTagCnnctPtABCD** ou **visTagCnnctNamedABCD**. As linhas estendidas podem ser identificadas pela presença de uma fórmula na célula D. 
  
 Você pode adicionar várias Connections.  *name* quantas forem necessárias, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar um ponto de conexão à uma seção Connection Points existente, clique com o botão direito em uma linha e clique **Inserir Linha** no menu de atalho. 
  
Você pode fazer referência as células de linha Connection Point pelo nome da linha, que aparece na janela ShapeSheet em texto vermelho. Para alterar o nome da linha, clique na linha e digite um nome, como *Custom*, por exemplo, para criar o nome da linha Connections.Custom. Você pode fazer referência à célula X usando Connections.Custom.X, por exemplo, ou Connections.X1 se quiser utilizar o número da linha. 
  
O nome de linha que você inserir deve ser único dentro da seção. Quando você cria um nome para uma linha na seção Connection Points, o Microsoft Office Visio nomeia todas as linhas da seção com o nome padrão, Connections.Row_*n*. 
  
As linhas Connection Points nomeadas não são compatíveis com versões do Visio anteriores ao Visio 5.0. Ao salvar um arquivo de desenho do Visio com linhas Connection Points nomeadas para um formato anterior, as referências às linhas Connection Points nomeadas são convertidas em referências indexadas e os nomes das linhas são perdidos.
  

