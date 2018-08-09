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
description: Contém os x e y-coordenadas, direção horizontal e vertical e tipo para uma conexão único ponto em uma forma. As coordenadas dos pontos de conexão são medidas em relação à origem da forma. Uma forma contém uma linha de pontos de Conexão para cada ponto de conexão.
ms.openlocfilehash: f1b8daf7f9845b85e76020c7f89c8c42b4500823
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771585"
---
# <a name="connection-points-row-connection-points-section"></a>Linha Connection Points (Seção Connection Points)

Contém os *x* e *y* -coordenadas, direção horizontal e vertical e tipo para uma conexão único ponto em uma forma. As coordenadas dos pontos de conexão são medidas em relação à origem da forma. Uma forma contém uma linha de pontos de Conexão para cada ponto de conexão. 
  
Se as linhas de pontos de Conexão são nomeadas, esses nomes aparecerão como Connections. *nome* na janela ShapeSheet. Linhas de pontos de Conexão contêm as células a seguir. Para obter mais detalhes, consulte os tópicos de célula específica. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |*X* -coordenadas de um ponto de conexão em coordenadas locais.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |*Y* -coordenadas de um ponto de conexão em coordenadas locais.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |*X* -component necessários vetor de alinhamento de um ponto de conexão coincidente. Ele também é usado para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |*Y* -component necessários vetor de alinhamento de um ponto de conexão coincidente. Ele também é usado para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto.  <br/> |
|[Tipo/C](typec-cell-connection-points-section.md) <br/> |O tipo de ponto de conexão (0 = para dentro; 1 = para fora; 2 = para dentro + para fora).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas. Para acessar essa célula, clique com o botão direito do mouse em uma linha e clique em **Alterar Tipo de Linha **no menu de atalho.<br/> |
   
## <a name="remarks"></a>Comentários

Células nas conexões. *nome da* linha são rotuladas DirX/A, DirY/B e Type/C porque essas linhas podem ser estendidas ou não-estendidas linhas. 
  
A maioria dos pontos de conexão (todos os pontos de conexão criados pela interface do usuário) é não-estendida e contém células DirX, DirY e Type. Seus tipos de linha são **visTagCnnctPt** ou **visTagCnnctNamed**.
  
Em linhas não-estendidas, as células DirX e DirY juntas definem um vetor de direção que influencia a rotação de formas envolvidas em conexões usando o ponto de conexão. Se ambas forem zero, o ponto não terá direção. Os pontos de conexão são do seguinte tipo:
  
- Para dentro (0), o que significa que as formas são coladas a ele. Esse é o padrão.
    
- Para fora (1), o que significa que esses pontos de conexão serão colados a pontos de conexão para dentro.
    
- Tanto para dentro como para fora (2), caso em que a direção é para dentro, sendo revertida se usada como uma conexão para fora.
    
As linhas estendidas contêm células A, B, C e D e se comportam como as linhas não-estendidas sem direção do tipo Para dentro. Normalmente, as linhas estendidas não são utilizadas, mas você pode precisar usá-las para associar os dados a um ponto de conexão nas células A, B, C e D. Seu tipo de linha é **visTagCnnctPtABCD** ou **visTagCnnctNamedABCD**. As linhas estendidas podem ser identificadas pela presença de uma fórmula na célula D. 
  
 Você pode adicionar tantos conexões.  linhas de *nome* conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar um ponto de conexão a uma seção de pontos de Conexão existente, do mouse em uma linha e clique em **Inserir linha** no menu de atalho. 
  
Você pode fazer referência a células da linha de pontos de Conexão pelo nome da linha, exibido em uma janela ShapeSheet em texto vermelho. Para alterar o nome da linha, clique nele e, em seguida, digite um nome como *personalizado* , por exemplo, para criar o nome da linha Custom. Você pode fazer referência à célula X usando Connections.X1 ou Connections.Custom.X, por exemplo, se você quiser usar o número da linha. 
  
O nome de linha inserido deve ser único na seção. Quando você cria um nome para uma linha na seção pontos de Conexão, o Microsoft Office Visio nomeia todas as linhas na seção com o nome padrão, Row _ *n* . 
  
As linhas Connection Points nomeadas não são compatíveis com versões do Visio anteriores ao Visio 5.0. Ao salvar um arquivo de desenho do Visio com linhas Connection Points nomeadas para um formato anterior, as referências às linhas Connection Points nomeadas são convertidas em referências indexadas e os nomes das linhas são perdidos.
  

