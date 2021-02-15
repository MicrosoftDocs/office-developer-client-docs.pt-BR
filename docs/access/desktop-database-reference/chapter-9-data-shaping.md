---
title: 'Capítulo 9: Data Shaping'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296420"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="1b325-102">Capítulo 9: Data Shaping</span><span class="sxs-lookup"><span data-stu-id="1b325-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="1b325-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b325-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b325-104">O *data shaping* permite consultar uma fonte de dados e retornar um [Recordset](recordset-object-ado.md) que representa uma relação pai-filho entre duas ou mais entidades lógicas (uma hierarquia).</span><span class="sxs-lookup"><span data-stu-id="1b325-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="1b325-105">Um exemplo clássico dessa relação envolve clientes e pedidos.</span><span class="sxs-lookup"><span data-stu-id="1b325-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="1b325-106">Para cada cliente em um banco de dados, é possível haver zero ou mais pedidos.</span><span class="sxs-lookup"><span data-stu-id="1b325-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="1b325-107">O SQL comum permite recuperar os dados com a sintaxe JOIN, mas isso pode ser ineficiente e difícil, pois os dados pai redundantes são repetidos em cada registro retornado para um relacionamento pai-filho específico.</span><span class="sxs-lookup"><span data-stu-id="1b325-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="1b325-108">O data shaping pode relacionar um único registro pai no **Recordset** pai a vários registros filho no **Recordset** filho, evitando a redundância de um JOIN.</span><span class="sxs-lookup"><span data-stu-id="1b325-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="1b325-109">A maioria das pessoas considera o modelo de programação de vários **Recordsets** pai-filho mais natural e fácil de trabalhar do que com o único modelo JOIN de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1b325-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="1b325-p102">A sintaxe do data shaping também permite outras possibilidades. Os desenvolvedores podem criar novos objetos **Recordset** sem qualquer fonte de dados subjacente, usando a palavra-chave NEW para descrever os campos dos **Recordsets** pai e filho. O novo objeto **Recordset** pode ser preenchido com dados e mantido de forma persistente. Os desenvolvedores também pode efetuar diversos cálculos ou agregados (por exemplo, SUM, AVG e MAX) nos campos filho. O data shaping também pode criar um **Recordset** pai a partir de um **Recordset** filho, agrupando registros no filho e inserindo uma linha no pai para cada grupo no filho.</span><span class="sxs-lookup"><span data-stu-id="1b325-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="1b325-115">Consulte os tópicos a seguir para saber mais sobre o data shaping:</span><span class="sxs-lookup"><span data-stu-id="1b325-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="1b325-116">Provedores necessários para Data Shaping</span><span class="sxs-lookup"><span data-stu-id="1b325-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="1b325-117">Cláusula de cálculo de forma</span><span class="sxs-lookup"><span data-stu-id="1b325-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="1b325-118">Fabricação de conjuntos de registros hierárquicos</span><span class="sxs-lookup"><span data-stu-id="1b325-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="1b325-119">Acesso de linhas em um conjunto de registros hierárquico</span><span class="sxs-lookup"><span data-stu-id="1b325-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="1b325-120">Gramática formal de forma</span><span class="sxs-lookup"><span data-stu-id="1b325-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="1b325-121">Funções do Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="1b325-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="1b325-122">Cláusula Shape Append (ADO)</span><span class="sxs-lookup"><span data-stu-id="1b325-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="1b325-123">Data shaping (ADO)</span><span class="sxs-lookup"><span data-stu-id="1b325-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="1b325-124">Comandos shape em geral (ADO)</span><span class="sxs-lookup"><span data-stu-id="1b325-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

