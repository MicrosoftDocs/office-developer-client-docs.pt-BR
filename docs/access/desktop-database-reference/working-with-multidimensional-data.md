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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306038"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="ce705-102">Como trabalhar com dados multidimensionais</span><span class="sxs-lookup"><span data-stu-id="ce705-102">Working with multidimensional data</span></span>

<span data-ttu-id="ce705-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce705-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce705-p101">Um *conjunto de células* é o resultado de uma consulta em dados multidimensionais. Ele consiste de uma coleção de eixos, em geral não mais do que quatro eixos e usualmente dois ou três. Um *eixo* é uma coleção de membros de uma ou mais dimensões, que é usada para localizar ou filtrar valores específicos em um cubo.</span><span class="sxs-lookup"><span data-stu-id="ce705-p101">A *cellset* is the result of a query on multidimensional data. It consists of a collection of axes, usually no more than four axes and typically only two or three. An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="ce705-p102">Uma *posição* é um ponto ao longo de um eixo. Para um eixo que consiste de uma única dimensão, essas posições são um subconjunto dos membros da dimensão. Se um eixo consiste de mais de uma dimensão, cada posição é uma entidade composta, que tem *n* partes, em que *n* é o número de dimensões orientadas ao longo daquele eixo. Cada parte da posição é um membro de uma dimensão constituinte.</span><span class="sxs-lookup"><span data-stu-id="ce705-p102">A *position* is a point along an axis. For an axis consisting of a single dimension, these positions are a subset of the dimension members. If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis. Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="ce705-p103">Por exemplo, se as dimensões Geografia e Produto de um cubo que contém dados de vendas estiverem orientadas ao longo do eixo x de um conjunto de células, uma posição ao longo desse eixo pode conter os membros "Estados Unidos" e "Computadores". Nesse exemplo, determinar uma posição ao longo do eixo x requer que os membros de cada dimensão estejam orientados ao longo do eixo.</span><span class="sxs-lookup"><span data-stu-id="ce705-p103">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers." In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="ce705-p104">Uma *célula* é um objeto posicionado na interseção de coordenadas do eixo. Cada célula tem várias informações a ela associadas, inclusive os próprios dados, uma sequência de caracteres formatada (a forma a ser exibida dos dados da célula) e o valor ordinal da célula. (Cada célula tem um valor ordinal único no conjunto de células. O valor ordinal da primeira célula no conjunto de células é zero, enquanto a célula mais à esquerda da segunda linha de um conjunto de células com oito colunas teria um valor ordinal igual a oito.)</span><span class="sxs-lookup"><span data-stu-id="ce705-p104">A *cell* is an object positioned at the intersection of axis coordinates. Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value. (Each cell is a unique ordinal value in the cellset. The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="ce705-117">Por exemplo, um cubo tem as seis dimensões a seguir (observe que esse esquema de cubo difere ligeiramente do exemplo dado em [Visão geral de esquemas e dados multidimensionais](overview-of-multidimensional-schemas-and-data.md)):</span><span class="sxs-lookup"><span data-stu-id="ce705-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="ce705-118">Vendedor</span><span class="sxs-lookup"><span data-stu-id="ce705-118">Salesperson</span></span>
- <span data-ttu-id="ce705-119">Geografia (hierarquia natural)  Continentes, Países, Estados e assim por diante</span><span class="sxs-lookup"><span data-stu-id="ce705-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="ce705-120">Trimestres  Trimestres, Meses, Dias</span><span class="sxs-lookup"><span data-stu-id="ce705-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="ce705-121">Anos</span><span class="sxs-lookup"><span data-stu-id="ce705-121">Years</span></span>
- <span data-ttu-id="ce705-122">Medidas  Vendas, AlteraçãoPercentual, VendasEstimadas</span><span class="sxs-lookup"><span data-stu-id="ce705-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="ce705-123">Produtos</span><span class="sxs-lookup"><span data-stu-id="ce705-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="ce705-124">[!OBSERVAçãO] O valores da célula no exemplo podem ser exibidos como pares ordenados de ordinais de posição do eixo, em que o primeiro dígito representa a posição do eixo x e o segundo dígito a posição do eixo y.</span><span class="sxs-lookup"><span data-stu-id="ce705-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="ce705-125">As características deste conjunto de células são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="ce705-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="ce705-126">Dimensões dos eixos: Trimestres, Vendedor, Geografia</span><span class="sxs-lookup"><span data-stu-id="ce705-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="ce705-127">Dimensões de filtro: Medidas, Anos, Produtos</span><span class="sxs-lookup"><span data-stu-id="ce705-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="ce705-128">Dois eixos: COLUNA (x ou Eixo 0) e LINHA (y ou Eixo 1)</span><span class="sxs-lookup"><span data-stu-id="ce705-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="ce705-129">eixo x: duas dimensões aninhadas, Vendedor e Geografia</span><span class="sxs-lookup"><span data-stu-id="ce705-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="ce705-130">eixo y: Dimensão de trimestres</span><span class="sxs-lookup"><span data-stu-id="ce705-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="ce705-p105">O eixo x tem duas dimensões aninhadas: Vendedor e Geografia. De Geografia, quatro membros são selecionados: Seattle, Boston, USA-South e Japan. Dois membros são selecionados de Vendedor: Valentine e Nash. Isso resulta em um total de oito posições nesse eixo (8 = 4\*2).</span><span class="sxs-lookup"><span data-stu-id="ce705-p105">The x-axis has two nested dimensions: Salesperson and Geography. From Geography, four members are selected: Seattle, Boston, USA-South, and Japan. Two members are selected from Salesperson: Valentine and Nash. This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="ce705-135">Cada coordenada é representada como uma posição com dois membros  um da dimensão Vendedor e outro da dimensão Geografia:</span><span class="sxs-lookup"><span data-stu-id="ce705-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="ce705-136">O eixo y tem apenas uma dimensão, contendo as oito posições a seguir:</span><span class="sxs-lookup"><span data-stu-id="ce705-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="ce705-137">Conjuntos de células, células, eixos e posições são todos representados no ADO MD por objetos correspondentes: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) e [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ce705-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

