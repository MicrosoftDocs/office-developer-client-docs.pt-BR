---
title: Como trabalhar com dados multidimensionais
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726068"
---
# <a name="working-with-multidimensional-data"></a>Como trabalhar com dados multidimensionais

**Aplica-se a**: Access 2013, o Office 2013

Um *conjunto de células* é o resultado de uma consulta de dados multidimensionais. Ele consiste de uma coleção de eixos, em geral não mais do que quatro eixos e usualmente dois ou três. Um *eixo* é uma coleção de membros de uma ou mais dimensões, que é usada para localizar ou filtrar valores específicos em um cubo.

Uma *posição* é um ponto em um eixo. Para um eixo que consiste de uma única dimensão, essas posições são um subconjunto dos membros da dimensão. Se um eixo consistir em mais de uma dimensão, cada posição é uma entidade composta, que tem partes *n* onde *n* é o número de dimensões orientada ao longo do eixo. Cada parte da posição é um membro de uma dimensão constituinte.

Por exemplo, se as dimensões Geografia e Produto de um cubo que contém dados de vendas estiverem orientadas ao longo do eixo x de um conjunto de células, uma posição ao longo desse eixo pode conter os membros "Estados Unidos" e "Computadores". Nesse exemplo, determinar uma posição ao longo do eixo x requer que os membros de cada dimensão estejam orientados ao longo do eixo.

Uma *célula* é um objeto posicionado na interseção de coordenadas de eixo. Cada célula tem várias informações a ela associadas, inclusive os próprios dados, uma sequência de caracteres formatada (a forma a ser exibida dos dados da célula) e o valor ordinal da célula. (Cada célula tem um valor ordinal único no conjunto de células. O valor ordinal da primeira célula no conjunto de células é zero, enquanto a célula mais à esquerda da segunda linha de um conjunto de células com oito colunas teria um valor ordinal igual a oito.)

Por exemplo, um cubo tem as seis dimensões a seguir (observe que esse esquema de cubo difere ligeiramente do exemplo dado em [Visão geral de esquemas e dados multidimensionais](overview-of-multidimensional-schemas-and-data.md)):

- Vendedor
- Geografia (hierarquia natural)  Continentes, Países, Estados e assim por diante
- Trimestres  Trimestres, Meses, Dias
- Anos
- Medidas  Vendas, AlteraçãoPercentual, VendasEstimadas
- Produtos

> [!NOTE]
> [!OBSERVAçãO] O valores da célula no exemplo podem ser exibidos como pares ordenados de ordinais de posição do eixo, em que o primeiro dígito representa a posição do eixo x e o segundo dígito a posição do eixo y.

As características deste conjunto de células são as seguintes:

- Dimensões dos eixos: Trimestres, Vendedor, Geografia

- Dimensões de filtro: Medidas, Anos, Produtos

- Dois eixos: COLUNA (x ou Eixo 0) e LINHA (y ou Eixo 1)

- eixo x: duas dimensões aninhadas, Vendedor e Geografia

- eixo y: Dimensão de trimestres

O eixo x tem duas dimensões aninhadas: Vendedor e Geografia. De Geografia, quatro membros são selecionados: Seattle, Boston, USA-South e Japan. Dois membros são selecionados de Vendedor: Valentine e Nash. Isso resulta em um total de oito posições nesse eixo (8 = 4\*2).

Cada coordenada é representada como uma posição com dois membros  um da dimensão Vendedor e outro da dimensão Geografia:

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

O eixo y tem apenas uma dimensão, contendo as oito posições a seguir:

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

Conjuntos de células, células, eixos e posições são todos representados no ADO MD por objetos correspondentes: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) e [Position](position-object-ado-md.md).

