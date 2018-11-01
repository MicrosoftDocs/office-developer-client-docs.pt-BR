---
title: Visão geral de esquemas e dados multidimensionais
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 376d80bc79af772cfd09b6f5b8759321ed4431ee
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887163"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>Visão geral de esquemas e dados multidimensionais


**Aplica-se a**: Access 2013, o Office 2013

## <a name="understanding-multidimensional-schemas"></a>Noções básicas sobre esquemas multidimensionais

O objeto de metadados central no ADO MD é o *cubo*, que consiste de um conjunto estruturado de dimensões, hierarquias, níveis e membros relacionados.

Uma *dimensão* é uma categoria independente dos dados do banco de dados multidimensional, derivado do seus entidades de negócios. Uma dimensão geralmente contém itens a serem usados como critérios de consulta para as medidas do banco de dados.

Uma *hierarquia* é um caminho de agregação de uma dimensão. Uma dimensão pode ter vários níveis de granularidade, que têm relações pai-filho. Uma hierarquia define como esses níveis são relacionados.

Um *nível* é uma etapa de agregação em uma hierarquia. Para dimensões com várias camadas de informações, cada camada é um nível.

*Membro* é um item de dados em uma dimensão. Geralmente, você cria uma legenda ou descreve uma medida do banco de dados usando membros.

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


  - Continentes = {North America, Europe}


  - Países = {Canada, USA, UK, Germany}


  - Regiões = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


  - Cidades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>Membros

Os membros do nível folha de uma hierarquia não têm filhos e os membros do nível raiz não têm pais. Todos os outros membros têm pelo menos um pai e um filho. Por exemplo, uma transversal parcial da árvore da hierarquia na dimensão Geografia resulta nas seguintes relações pai-filho:

  - {All} (pai) {Europa, América do Norte}

  - {North America} (pai) {Canadá, EUA}

  - {EUA} (pai) {USA-NE, USA-NW, USA-SE, USA-SW}

  - {USA-NW} (pai) {Seattle, Boise}

Os membros podem ser consolidados ao longo de uma ou mais hierarquias por dimensão.

Esse exemplo também ilustra outra característica: alguns membros do nível Semana da hierarquia Ano-Semana não aparecem em qualquer nível da hierarquia Ano-Trimestre. Portanto, uma hierarquia não precisa incluir todos os membros de uma dimensão.

## <a name="understanding-multidimensional-schemas"></a>Noções básicas sobre esquemas multidimensionais

O objeto de metadados central no ADO MD é o *cubo*, que consiste de um conjunto estruturado de dimensões, hierarquias, níveis e membros relacionados.

Uma *dimensão* é uma categoria independente dos dados do banco de dados multidimensional, derivado do seus entidades de negócios. Uma dimensão geralmente contém itens a serem usados como critérios de consulta para as medidas do banco de dados.

Uma *hierarquia* é um caminho de agregação de uma dimensão. Uma dimensão pode ter vários níveis de granularidade, que têm relações pai-filho. Uma hierarquia define como esses níveis são relacionados.

Um *nível* é uma etapa de agregação em uma hierarquia. Para dimensões com várias camadas de informações, cada camada é um nível.

*Membro* é um item de dados em uma dimensão. Geralmente, você cria uma legenda ou descreve uma medida do banco de dados usando membros.

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


- Continentes = {North America, Europe}


- Países = {Canada, USA, UK, Germany}


- Regiões = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


- Cidades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>Membros

Os membros do nível folha de uma hierarquia não têm filhos e os membros do nível raiz não têm pais. Todos os outros membros têm pelo menos um pai e um filho. Por exemplo, uma transversal parcial da árvore da hierarquia na dimensão Geografia resulta nas seguintes relações pai-filho:

- {All} (pai) {Europa, América do Norte}

- {North America} (pai) {Canadá, EUA}

- {EUA} (pai) {USA-NE, USA-NW, USA-SE, USA-SW}

- {USA-NW} (pai) {Seattle, Boise}

Os membros podem ser consolidados ao longo de uma ou mais hierarquias por dimensão.

Esse exemplo também ilustra outra característica: alguns membros do nível Semana da hierarquia Ano-Semana não aparecem em qualquer nível da hierarquia Ano-Trimestre. Portanto, uma hierarquia não precisa incluir todos os membros de uma dimensão.

