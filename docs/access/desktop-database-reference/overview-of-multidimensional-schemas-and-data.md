---
title: Visão geral de esquemas e dados multidimensionais
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ce7366437028ed1e745c596c38b2c0314acefd2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945890"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="3b1f7-102">Visão geral de esquemas e dados multidimensionais</span><span class="sxs-lookup"><span data-stu-id="3b1f7-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="3b1f7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b1f7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="3b1f7-104">Noções básicas sobre esquemas multidimensionais</span><span class="sxs-lookup"><span data-stu-id="3b1f7-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="3b1f7-105">O objeto de metadados central no ADO MD é o *cubo*, que consiste de um conjunto estruturado de dimensões, hierarquias, níveis e membros relacionados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="3b1f7-106">Uma *dimensão* é uma categoria independente dos dados do banco de dados multidimensional, derivado do seus entidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="3b1f7-107">Uma dimensão geralmente contém itens a serem usados como critérios de consulta para as medidas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="3b1f7-108">Uma *hierarquia* é um caminho de agregação de uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="3b1f7-109">Uma dimensão pode ter vários níveis de granularidade, que têm relações pai-filho.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="3b1f7-110">Uma hierarquia define como esses níveis são relacionados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="3b1f7-111">Um *nível* é uma etapa de agregação em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="3b1f7-112">Para dimensões com várias camadas de informações, cada camada é um nível.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="3b1f7-113">*Membro* é um item de dados em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="3b1f7-114">Geralmente, você cria uma legenda ou descreve uma medida do banco de dados usando membros.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="3b1f7-p105">Cubos são representados por objetos [CubeDef](cubedef-object-ado-md.md) no ADO MD. Dimensões, hierarquias, níveis e membros são representados também por seus objetos ADO MD correspondentes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) e [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="3b1f7-117">Dimensões</span><span class="sxs-lookup"><span data-stu-id="3b1f7-117">Dimensions</span></span>

<span data-ttu-id="3b1f7-p106">As dimensões de um cubo dependem de suas entidades comerciais e dos tipos de dados a serem modelados no banco de dados. Geralmente, cada dimensão é um ponto de entrada ou mecanismo independente para selecionar dados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="3b1f7-p107">Por exemplo, um cubo que contenha dados de vendas tem as seguintes cinco dimensões: Vendedor, Geografia, Horário, Produtos e Medidas. A dimensão Medidas contém valores reais de dados de vendas, enquanto as outras dimensões representam maneiras de categorizar e agrupar os valores de dados de vendas.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="3b1f7-122">A dimensão Geografia tem o seguinte conjunto de membros:</span><span class="sxs-lookup"><span data-stu-id="3b1f7-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="3b1f7-123">Hierarquias</span><span class="sxs-lookup"><span data-stu-id="3b1f7-123">Hierarchies</span></span>

<span data-ttu-id="3b1f7-p108">As hierarquias definem as maneiras nas quais os níveis de uma dimensão podem ser "acumulados" ou agrupados. Uma dimensão pode ter mais de uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="3b1f7-126">Níveis</span><span class="sxs-lookup"><span data-stu-id="3b1f7-126">Levels</span></span>

<span data-ttu-id="3b1f7-127">No exemplo da dimensão Geografia descrito na figura anterior, cada caixa representa um nível na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="3b1f7-128">Cada nível tem um conjunto de membros, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="3b1f7-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="3b1f7-129">O Mundo = {All}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-129">The World = {All}</span></span>

  - <span data-ttu-id="3b1f7-130">Continentes = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="3b1f7-131">Países = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="3b1f7-132">Regiões = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="3b1f7-133">Cidades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="3b1f7-134">Membros</span><span class="sxs-lookup"><span data-stu-id="3b1f7-134">Members</span></span>

<span data-ttu-id="3b1f7-p109">Os membros do nível folha de uma hierarquia não têm filhos e os membros do nível raiz não têm pais. Todos os outros membros têm pelo menos um pai e um filho. Por exemplo, uma transversal parcial da árvore da hierarquia na dimensão Geografia resulta nas seguintes relações pai-filho:</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="3b1f7-138">{All} (pai) {Europa, América do Norte}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="3b1f7-139">{North America} (pai) {Canadá, EUA}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="3b1f7-140">{EUA} (pai) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="3b1f7-141">{USA-NW} (pai) {Seattle, Boise}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="3b1f7-142">Os membros podem ser consolidados ao longo de uma ou mais hierarquias por dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="3b1f7-143">Este exemplo também ilustra outra característica: alguns membros do nível da hierarquia da semana do ano semana não aparecem em qualquer nível da hierarquia trimestre do ano.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="3b1f7-144">Portanto, uma hierarquia não precisa incluir todos os membros de uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="3b1f7-145">Noções básicas sobre esquemas multidimensionais</span><span class="sxs-lookup"><span data-stu-id="3b1f7-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="3b1f7-146">O objeto de metadados central no ADO MD é o *cubo*, que consiste de um conjunto estruturado de dimensões, hierarquias, níveis e membros relacionados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="3b1f7-147">Uma *dimensão* é uma categoria independente dos dados do banco de dados multidimensional, derivado do seus entidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="3b1f7-148">Uma dimensão geralmente contém itens a serem usados como critérios de consulta para as medidas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="3b1f7-149">Uma *hierarquia* é um caminho de agregação de uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="3b1f7-150">Uma dimensão pode ter vários níveis de granularidade, que têm relações pai-filho.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="3b1f7-151">Uma hierarquia define como esses níveis são relacionados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="3b1f7-152">Um *nível* é uma etapa de agregação em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="3b1f7-153">Para dimensões com várias camadas de informações, cada camada é um nível.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="3b1f7-154">*Membro* é um item de dados em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="3b1f7-155">Geralmente, você cria uma legenda ou descreve uma medida do banco de dados usando membros.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="3b1f7-p115">Cubos são representados por objetos [CubeDef](cubedef-object-ado-md.md) no ADO MD. Dimensões, hierarquias, níveis e membros são representados também por seus objetos ADO MD correspondentes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) e [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="3b1f7-158">Dimensões</span><span class="sxs-lookup"><span data-stu-id="3b1f7-158">Dimensions</span></span>

<span data-ttu-id="3b1f7-p116">As dimensões de um cubo dependem de suas entidades comerciais e dos tipos de dados a serem modelados no banco de dados. Geralmente, cada dimensão é um ponto de entrada ou mecanismo independente para selecionar dados.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="3b1f7-p117">Por exemplo, um cubo que contenha dados de vendas tem as seguintes cinco dimensões: Vendedor, Geografia, Horário, Produtos e Medidas. A dimensão Medidas contém valores reais de dados de vendas, enquanto as outras dimensões representam maneiras de categorizar e agrupar os valores de dados de vendas.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="3b1f7-163">A dimensão Geografia tem o seguinte conjunto de membros:</span><span class="sxs-lookup"><span data-stu-id="3b1f7-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="3b1f7-164">Hierarquias</span><span class="sxs-lookup"><span data-stu-id="3b1f7-164">Hierarchies</span></span>

<span data-ttu-id="3b1f7-p118">As hierarquias definem as maneiras nas quais os níveis de uma dimensão podem ser "acumulados" ou agrupados. Uma dimensão pode ter mais de uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="3b1f7-167">Níveis</span><span class="sxs-lookup"><span data-stu-id="3b1f7-167">Levels</span></span>

<span data-ttu-id="3b1f7-168">No exemplo da dimensão Geografia descrito na figura anterior, cada caixa representa um nível na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="3b1f7-169">Cada nível tem um conjunto de membros, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="3b1f7-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="3b1f7-170">O Mundo = {All}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-170">The World = {All}</span></span>

- <span data-ttu-id="3b1f7-171">Continentes = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="3b1f7-172">Países = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="3b1f7-173">Regiões = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="3b1f7-174">Cidades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="3b1f7-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="3b1f7-175">Membros</span><span class="sxs-lookup"><span data-stu-id="3b1f7-175">Members</span></span>

<span data-ttu-id="3b1f7-p119">Os membros do nível folha de uma hierarquia não têm filhos e os membros do nível raiz não têm pais. Todos os outros membros têm pelo menos um pai e um filho. Por exemplo, uma transversal parcial da árvore da hierarquia na dimensão Geografia resulta nas seguintes relações pai-filho:</span><span class="sxs-lookup"><span data-stu-id="3b1f7-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="3b1f7-179">{All} (pai) {Europa, América do Norte}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="3b1f7-180">{North America} (pai) {Canadá, EUA}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="3b1f7-181">{EUA} (pai) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="3b1f7-182">{USA-NW} (pai) {Seattle, Boise}</span><span class="sxs-lookup"><span data-stu-id="3b1f7-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="3b1f7-183">Os membros podem ser consolidados ao longo de uma ou mais hierarquias por dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="3b1f7-184">Este exemplo também ilustra outra característica: alguns membros do nível da hierarquia da semana do ano semana não aparecem em qualquer nível da hierarquia trimestre do ano.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="3b1f7-185">Portanto, uma hierarquia não precisa incluir todos os membros de uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

