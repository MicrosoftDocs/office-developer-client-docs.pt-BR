---
title: Visão geral de dados e esquemas multidimensionais
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288151"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>Visão geral de dados e esquemas multidimensionais

**Aplica-se ao:** Access 2013, Office 2013

## <a name="understanding-multidimensional-schemas"></a>Noções básicas sobre esquemas multidimensionais

O objeto de metadados central no ADO MD é o *cubo*, que consiste de um conjunto estruturado de dimensões, hierarquias, níveis e membros relacionados.

Uma *dimensão* é uma categoria independente de dados de seu banco de dados multidimensional, derivados de suas entidades comerciais. Uma dimensão geralmente contém itens a serem usados como critérios de consulta para as medidas do banco de dados.

Uma *hierarquia* é um caminho de agregação de uma dimensão. Uma dimensão pode ter vários níveis de granularidade, que têm relações pai-filho. Uma hierarquia define como esses níveis são relacionados.

Um *nível* é uma etapa de agregação em uma hierarquia. Para dimensões com várias camadas de informações, cada camada é um nível.

Um *membro* é um item de dados em uma dimensão. Geralmente, você cria uma legenda ou descreve uma medida do banco de dados usando membros.

Cubos são representados por objetos [CubeDef](cubedef-object-ado-md.md) no ADO MD. Dimensões, hierarquias, níveis e membros são representados também por seus objetos ADO MD correspondentes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) e [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensões

As dimensões de um cubo dependem de suas entidades comerciais e dos tipos de dados a serem modelados no banco de dados. Geralmente, cada dimensão é um ponto de entrada ou mecanismo independente para selecionar dados.

Por exemplo, um cubo que contenha dados de vendas tem as seguintes cinco dimensões: Vendedor, Geografia, Horário, Produtos e Medidas. A dimensão Medidas contém valores reais de dados de vendas, enquanto as outras dimensões representam maneiras de categorizar e agrupar os valores de dados de vendas.

A dimensão Geografia tem o seguinte conjunto de membros:

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hierarquias

As hierarquias definem as maneiras nas quais os níveis de uma dimensão podem ser "acumulados" ou agrupados. Uma dimensão pode ter mais de uma hierarquia.

## <a name="levels"></a>Níveis

No exemplo da dimensão Geografia descrito na figura anterior, cada caixa representa um nível na hierarquia.

Cada nível tem um conjunto de membros, conforme mostrado a seguir:

  - O Mundo = {All}


  - Continentes = {América do Norte, Europa}

  - Países = {Canadá, EUA, ru, Alemanha}

  - Regions = {Canada-leste, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, Inglaterra, Irlanda, Escócia, Gales, Alemanha-Norte, Alemanha-Sul}

  - Cidades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, Nova York, London, Dover, Glasgow, Edimburgo, Cardiff, Pembroke, Belfast, Berlim, Hamburg, Munique, Stuttgart}

## <a name="members"></a>Members

Os membros do nível folha de uma hierarquia não têm filhos e os membros do nível raiz não têm pais. Todos os outros membros têm pelo menos um pai e um filho. Por exemplo, uma transversal parcial da árvore da hierarquia na dimensão Geografia resulta nas seguintes relações pai-filho:

- Todos os (pai de) {Europa, América do Norte}
- {América do Norte} (pai de) {Canadá, USA}
- Japão (pai de) {USA-NE, USA-NW, USA-SE, USA-SW}
- {USA-NW} (pai de) {Boise, Seattle}

Os membros podem ser consolidados ao longo de uma ou mais hierarquias por dimensão.

Este exemplo também ilustra outra característica: alguns membros do nível semana da hierarquia ano-semana não aparecem em qualquer nível da hierarquia ano-trimestre. Portanto, uma hierarquia não precisa incluir todos os membros de uma dimensão.

## <a name="understanding-multidimensional-schemas"></a>Noções básicas sobre esquemas multidimensionais

O objeto de metadados central no ADO MD é o *cubo*, que consiste de um conjunto estruturado de dimensões, hierarquias, níveis e membros relacionados.

Uma *dimensão* é uma categoria independente de dados de seu banco de dados multidimensional, derivados de suas entidades comerciais. Uma dimensão geralmente contém itens a serem usados como critérios de consulta para as medidas do banco de dados.

Uma *hierarquia* é um caminho de agregação de uma dimensão. Uma dimensão pode ter vários níveis de granularidade, que têm relações pai-filho. Uma hierarquia define como esses níveis são relacionados.

Um *nível* é uma etapa de agregação em uma hierarquia. Para dimensões com várias camadas de informações, cada camada é um nível.

Um *membro* é um item de dados em uma dimensão. Geralmente, você cria uma legenda ou descreve uma medida do banco de dados usando membros.

Cubos são representados por objetos [CubeDef](cubedef-object-ado-md.md) no ADO MD. Dimensões, hierarquias, níveis e membros são representados também por seus objetos ADO MD correspondentes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) e [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensões

As dimensões de um cubo dependem de suas entidades comerciais e dos tipos de dados a serem modelados no banco de dados. Geralmente, cada dimensão é um ponto de entrada ou mecanismo independente para selecionar dados.

Por exemplo, um cubo que contenha dados de vendas tem as seguintes cinco dimensões: Vendedor, Geografia, Horário, Produtos e Medidas. A dimensão Medidas contém valores reais de dados de vendas, enquanto as outras dimensões representam maneiras de categorizar e agrupar os valores de dados de vendas.

A dimensão Geografia tem o seguinte conjunto de membros:

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hierarquias

As hierarquias definem as maneiras nas quais os níveis de uma dimensão podem ser "acumulados" ou agrupados. Uma dimensão pode ter mais de uma hierarquia.

## <a name="levels"></a>Níveis

No exemplo da dimensão Geografia descrito na figura anterior, cada caixa representa um nível na hierarquia.

Cada nível tem um conjunto de membros, conforme mostrado a seguir:

- O Mundo = {All}


- Continentes = {América do Norte, Europa}

- Países = {Canadá, EUA, ru, Alemanha}

- Regions = {Canada-leste, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, Inglaterra, Irlanda, Escócia, Gales, Alemanha-Norte, Alemanha-Sul}

- Cidades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, Nova York, London, Dover, Glasgow, Edimburgo, Cardiff, Pembroke, Belfast, Berlim, Hamburg, Munique, Stuttgart}

## <a name="members"></a>Members

Os membros do nível folha de uma hierarquia não têm filhos e os membros do nível raiz não têm pais. Todos os outros membros têm pelo menos um pai e um filho. Por exemplo, uma transversal parcial da árvore da hierarquia na dimensão Geografia resulta nas seguintes relações pai-filho:

- Todos os (pai de) {Europa, América do Norte}

- {América do Norte} (pai de) {Canadá, USA}

- Japão (pai de) {USA-NE, USA-NW, USA-SE, USA-SW}

- {USA-NW} (pai de) {Boise, Seattle}

Os membros podem ser consolidados ao longo de uma ou mais hierarquias por dimensão.

Este exemplo também ilustra outra característica: alguns membros do nível semana da hierarquia ano-semana não aparecem em qualquer nível da hierarquia ano-trimestre. Portanto, uma hierarquia não precisa incluir todos os membros de uma dimensão.

