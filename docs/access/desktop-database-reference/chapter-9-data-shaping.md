---
title: 'Capítulo 9: Data shaping'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8217be1004ea8304501e7d32908b8af269873b7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464485"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="75af3-102">Capítulo 9: Data shaping</span><span class="sxs-lookup"><span data-stu-id="75af3-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="75af3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75af3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75af3-104">*Data shaping* fornece uma maneira para consultar uma fonte de dados e retornar um [Recordset](recordset-object-ado.md) que representa uma relação pai-filho entre dois ou mais entidades lógicas (uma hierarquia).</span><span class="sxs-lookup"><span data-stu-id="75af3-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="75af3-105">Um exemplo clássico dessa relação envolve clientes e pedidos.</span><span class="sxs-lookup"><span data-stu-id="75af3-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="75af3-106">Para cada cliente em um banco de dados, é possível haver zero ou mais pedidos.</span><span class="sxs-lookup"><span data-stu-id="75af3-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="75af3-107">O SQL comum permite recuperar os dados com a sintaxe JOIN, mas isso pode ser ineficiente e difícil, pois os dados pai redundantes são repetidos em cada registro retornado para um relacionamento pai-filho específico.</span><span class="sxs-lookup"><span data-stu-id="75af3-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="75af3-108">O data shaping pode relacionar um único registro pai no **Recordset** pai a vários registros filho no **Recordset** filho, evitando a redundância de um JOIN.</span><span class="sxs-lookup"><span data-stu-id="75af3-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="75af3-109">A maioria das pessoas considera o modelo de programação de vários **Recordsets** pai-filho mais natural e fácil de trabalhar do que com o único modelo JOIN de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="75af3-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="75af3-p102">A sintaxe do data shaping também permite outras possibilidades. Os desenvolvedores podem criar novos objetos **Recordset** sem qualquer fonte de dados subjacente, usando a palavra-chave NEW para descrever os campos dos **Recordsets** pai e filho. O novo objeto **Recordset** pode ser preenchido com dados e mantido de forma persistente. Os desenvolvedores também pode efetuar diversos cálculos ou agregados (por exemplo, SUM, AVG e MAX) nos campos filho. O data shaping também pode criar um **Recordset** pai a partir de um **Recordset** filho, agrupando registros no filho e inserindo uma linha no pai para cada grupo no filho.</span><span class="sxs-lookup"><span data-stu-id="75af3-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="75af3-115">Consulte os tópicos a seguir para saber mais sobre o data shaping:</span><span class="sxs-lookup"><span data-stu-id="75af3-115">See the following topics to learn more about data shaping:</span></span>

  - [<span data-ttu-id="75af3-116">Resumo do data shaping</span><span class="sxs-lookup"><span data-stu-id="75af3-116">Data Shaping Summary</span></span>](data-shaping-summary.md)

  - [<span data-ttu-id="75af3-117">Provedores necessários para o data shaping</span><span class="sxs-lookup"><span data-stu-id="75af3-117">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

  - [<span data-ttu-id="75af3-118">Comandos shape em geral</span><span class="sxs-lookup"><span data-stu-id="75af3-118">Shape Commands in General</span></span>](shape-commands-in-general.md)

  - [<span data-ttu-id="75af3-119">Cláusula Shape APPEND</span><span class="sxs-lookup"><span data-stu-id="75af3-119">Shape APPEND Clause</span></span>](shape-append-clause.md)

  - [<span data-ttu-id="75af3-120">Cláusula COMPUTE de forma</span><span class="sxs-lookup"><span data-stu-id="75af3-120">Shape COMPUTE Clause</span></span>](shape-compute-clause.md)

  - [<span data-ttu-id="75af3-121">Criando conjuntos de registros hierárquicos</span><span class="sxs-lookup"><span data-stu-id="75af3-121">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

  - [<span data-ttu-id="75af3-122">Acessando linhas em um conjunto de registros hierárquico</span><span class="sxs-lookup"><span data-stu-id="75af3-122">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

  - [<span data-ttu-id="75af3-123">Gramática formal de shape</span><span class="sxs-lookup"><span data-stu-id="75af3-123">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

  - [<span data-ttu-id="75af3-124">Funções do Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="75af3-124">Visual Basic for Applications Functions</span></span>](visual-basic-for-applications-functions.md)

