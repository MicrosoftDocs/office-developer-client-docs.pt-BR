---
title: Sobre a Planilha ShapeSheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251822
localization_priority: Normal
ms.assetid: f403890d-4a3a-bacc-53d7-1b9920b23639
description: Todos os elementos do Microsoft Visio, cada documento, página, estilo, forma, grupo, forma ou objeto em um grupo, mestre, objeto de outro programa, guia e ponto de guia têm uma planilha ShapeSheet na qual as informações sobre esse objeto são armazenadas. Essa planilha contém informações como altura, largura, ângulo, cor e outros atributos que determinam a aparência e o comportamento da forma.
ms.openlocfilehash: 37b2ae10b1f511197af5ccf739de91edb74e7819
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345146"
---
# <a name="about-the-shapesheet-spreadsheet"></a>Sobre a planilha ShapeSheet

Todos os elementos do Microsoft Visio, cada documento, página, estilo, forma, grupo, forma ou objeto em um grupo, mestre, objeto de outro programa, guia e ponto de guia têm uma planilha ShapeSheet na qual as informações sobre esse objeto são armazenadas. Essa planilha contém informações como altura, largura, ângulo, cor e outros atributos que determinam a aparência e o comportamento da forma.
  
Como desenvolvedor de formas, você precisa ter um controle preciso sobre a aparência e o comportamento das formas criadas. É possível alterar o comportamento padrão de uma forma e aprimorá-la editando-a em sua planilha ShapeSheet, que pode ser acessada em uma janela do ShapeSheet ou programaticamente.
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a>Exibir um objeto na janela do ShapeSheet

A janela de desenho Visio e a janela ShapeSheet são simplesmente diferentes visualizações da mesma forma.
  
- Ao exibir uma forma em uma janela de desenho, é possível visualizá-la processada graficamente e se comportando de acordo com as fórmulas de sua ShapeSheet.
    
- Quando uma forma é visualizada em uma janela ShapeSheet, é possível ver as fórmulas subjacentes que determinam como será a aparência e o comportamento da forma na página de desenho.
    
É possível exibir uma janela ShapeSheet e uma janela de desenho ao mesmo tempo e ver a alteração da forma na janela de desenho à medida que você manipula as células na janela ShapeSheet ou vice-versa. Por exemplo, quando você move a forma com o ponteiro, as fórmulas PinX e PinY da forma na seção Shape Transform mudam para refletir sua nova posição na página de desenho.
  
## <a name="structure-of-the-shapesheet-window"></a>Estrutura da janela ShapeSheet

Uma ShapeSheet estiver dividida em *seções* que controlam um aspecto específico de comportamento de uma forma ou a aparência, por exemplo, seu geometria ou a formatação. Cada seção inclui um ou mais *linhas* que contêm *células* . Cada célula pode conter uma fórmula, seu resultado (normalmente chamado de valor da célula) e informações de erro opcional. Uma fórmula pode ser necessária ou opcional, dependendo de cada célula. Os dados de uma célula (por exemplo, sua fórmula ou um valor) podem ser definidos localmente ou, com mais frequência, herdados através da célula equivalente no mestre de estilo da forma. 
  
O exemplo a seguir mostra a barra de fórmulas ![barra de fórmulas](media/callout1_ZA01036259.gif), uma seção. ![seção](media/callout2_ZA01036260.gif), uma célula ![célula](media/callout3_ZA01036261.gif), e uma linha ![row](media/callout4_ZA01036262.gif) na janela ShapeSheet. 
  
![janela ShapeSheet.](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
Quando você desenha uma forma, o Visio registra essa forma como um conjunto de locações horizontais e verticais conectadas com o segmentos de linha. Esses locais (chamados vértices) são gravados nas células X e Y da seção de**geometria** da forma. Conforme mostrado no exemplo a seguir, quando você clica em células X e Y na seção **geometria** de uma janela de forma ShapeSheet, você verá uma caixa com as bordas pretas, realçando o vértice de forma na janela de desenho. 
  
![Caixa com bordas pretas, realçando o vértice de forma na janela de desenho](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a>Editando um objeto na janela do ShapeSheet

Quando uma janela do ShapeSheet está ativa, a faixa de opções é alterada para exibir opções específicas ao trabalho nessa janela. Ao selecionar uma célula do ShapeSheet, é exibida uma barra de fórmulas, a qual é utilizada para inserir e editar as fórmulas de um objeto. Uma outra alternativa é trabalhar diretamente na célula.
  
Em uma janela de ShapeSheet, você pode adicionar seções a uma planilha de forma para adicionar novas características ao formato na página de desenho. Por exemplo, você pode adicionar uma seção**pontos de Conexão** para criar uma conexão. Quando não precisar de uma seção, você pode excluí-la. 
  
Você também pode adicionar linhas às seções para manter  fórmulas adicionais ou para alterar a aparência da forma. Por exemplo, você pode adicionar uma linha a uma seção **geometria**para adicionar um segmento de forma. Da mesma forma, você pode excluir linhas desnecessárias. 
  
Tanto fórmulas como valores podem ser exibidos nas células. Exiba as fórmulas quando estiver inserindo novas fórmulas, editando fórmulas existentes ou para visualizar como as fórmulas se relacionam entre si nas células. Um valor é o resultado obtido quando o Visio avalia a fórmula de uma célula. É possível exibir os valores nas células para ver o resultado de uma avaliação.
  
## <a name="additional-shapesheet-references"></a>Referências ShapeSheet adicionais

Para obter detalhes sobre uma seção em particular, uma linha ou uma célula com o ShapeSheet, confiar o artigo correspondente na referência [ShapeSheet](reference-visio-shapesheet.md).
  
Para obter detalhes sobre como acessar a planilha ShapeSheet por programação, consulte a referência de automação do Microsoft Visio.
  

