---
title: 'Capítulo 9: Data Shaping'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4636c853f58557b30474b78d902131329084a1a2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863882"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="c5e04-102">Capítulo 9: Data Shaping</span><span class="sxs-lookup"><span data-stu-id="c5e04-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="c5e04-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5e04-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c5e04-104">*Data shaping* fornece uma maneira para consultar uma fonte de dados e retornar um [Recordset](recordset-object-ado.md) que representa uma relação pai-filho entre dois ou mais entidades lógicas (uma hierarquia).</span><span class="sxs-lookup"><span data-stu-id="c5e04-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="c5e04-105">Um exemplo clássico dessa relação envolve clientes e pedidos.</span><span class="sxs-lookup"><span data-stu-id="c5e04-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="c5e04-106">Para cada cliente em um banco de dados, é possível haver zero ou mais pedidos.</span><span class="sxs-lookup"><span data-stu-id="c5e04-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="c5e04-107">O SQL comum permite recuperar os dados com a sintaxe JOIN, mas isso pode ser ineficiente e difícil, pois os dados pai redundantes são repetidos em cada registro retornado para um relacionamento pai-filho específico.</span><span class="sxs-lookup"><span data-stu-id="c5e04-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="c5e04-108">O data shaping pode relacionar um único registro pai no **Recordset** pai a vários registros filho no **Recordset** filho, evitando a redundância de um JOIN.</span><span class="sxs-lookup"><span data-stu-id="c5e04-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="c5e04-109">A maioria das pessoas considera o modelo de programação de vários **Recordsets** pai-filho mais natural e fácil de trabalhar do que com o único modelo JOIN de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c5e04-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="c5e04-p102">A sintaxe do data shaping também permite outras possibilidades. Os desenvolvedores podem criar novos objetos **Recordset** sem qualquer fonte de dados subjacente, usando a palavra-chave NEW para descrever os campos dos **Recordsets** pai e filho. O novo objeto **Recordset** pode ser preenchido com dados e mantido de forma persistente. Os desenvolvedores também pode efetuar diversos cálculos ou agregados (por exemplo, SUM, AVG e MAX) nos campos filho. O data shaping também pode criar um **Recordset** pai a partir de um **Recordset** filho, agrupando registros no filho e inserindo uma linha no pai para cada grupo no filho.</span><span class="sxs-lookup"><span data-stu-id="c5e04-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="c5e04-115">Consulte os tópicos a seguir para saber mais sobre o data shaping:</span><span class="sxs-lookup"><span data-stu-id="c5e04-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="c5e04-116">Provedores necessários para o data shaping</span><span class="sxs-lookup"><span data-stu-id="c5e04-116">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

- [<span data-ttu-id="c5e04-117">Cláusula Compute de forma</span><span class="sxs-lookup"><span data-stu-id="c5e04-117">Shape Compute Clause</span></span>](shape-compute-clause.md)

- [<span data-ttu-id="c5e04-118">Criando conjuntos de registros hierárquicos</span><span class="sxs-lookup"><span data-stu-id="c5e04-118">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

- [<span data-ttu-id="c5e04-119">Acessando linhas em um conjunto de registros hierárquico</span><span class="sxs-lookup"><span data-stu-id="c5e04-119">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

- [<span data-ttu-id="c5e04-120">Gramática formal de shape</span><span class="sxs-lookup"><span data-stu-id="c5e04-120">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

- [<span data-ttu-id="c5e04-121">Visual Basic para funções de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c5e04-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)

- [<span data-ttu-id="c5e04-122">(ADO) da cláusula Shape Append</span><span class="sxs-lookup"><span data-stu-id="c5e04-122">Shape Append Clause (ADO)</span></span>](shape-append-clause.md)

- [<span data-ttu-id="c5e04-123">Data Shaping (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5e04-123">Data Shaping (ADO)</span></span>](data-shaping.md)

- [<span data-ttu-id="c5e04-124">Comandos Shape em geral (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5e04-124">Shape Commands in General (ADO)</span></span>](shape-commands-in-general.md)

