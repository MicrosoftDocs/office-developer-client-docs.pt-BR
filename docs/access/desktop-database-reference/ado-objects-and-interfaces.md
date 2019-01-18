---
title: Objetos e interfaces do ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 539feb1918877189548d0e7cff6ceb28e50abddc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718858"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="7eabe-102">Objetos e interfaces do ADO</span><span class="sxs-lookup"><span data-stu-id="7eabe-102">ADO objects and interfaces</span></span>

<span data-ttu-id="7eabe-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7eabe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7eabe-104">As relações entre esses objetos são representadas no modelo de objeto do ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="7eabe-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="7eabe-105">Cada objeto pode estar contido em sua coleção correspondente.</span><span class="sxs-lookup"><span data-stu-id="7eabe-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="7eabe-106">Por exemplo, um objeto [Error](error-object-ado.md) pode estar contido em uma coleção [Errors](errors-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7eabe-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="7eabe-107">Para obter mais informações, consulte [coleções do ADO](ado-collections.md) ou um tópico da coleção específica.</span><span class="sxs-lookup"><span data-stu-id="7eabe-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="7eabe-108">Objeto</span><span class="sxs-lookup"><span data-stu-id="7eabe-108">Object</span></span></th>
<th><span data-ttu-id="7eabe-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7eabe-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eabe-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-111">Constrói um objeto <strong>Record</strong> do ADO a partir de um objeto <strong>Row</strong> do OLE DB em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="7eabe-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eabe-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-113">Constrói um objeto <strong>Recordset</strong> do ADO a partir de um objeto <strong>Rowset</strong> do OLE DB em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="7eabe-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eabe-114"><a href="error-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-115">Define um comando específico que você pretende executar em relação a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7eabe-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eabe-116"><a href="field-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-117">Representa uma conexão aberta com uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7eabe-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eabe-118"><a href="error-object-ado.md">Error</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-119">Contém os detalhes sobre os erros de acesso aos dados que pertencem à uma única operação que envolve o provedor.</span><span class="sxs-lookup"><span data-stu-id="7eabe-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eabe-120"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-121">Representa uma coluna de dados com um tipo de dados comuns.</span><span class="sxs-lookup"><span data-stu-id="7eabe-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eabe-122"><a href="parameter-object-ado.md">Parâmetro</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-123">Representa um parâmetro ou argumento associado ao objeto <strong>Command</strong> com base em uma consulta parametrizada ou em um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="7eabe-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eabe-124"><a href="property-object-ado.md">Property</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-125">Representa uma característica dinâmica de um objeto ADO definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="7eabe-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eabe-126"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-127">Representa uma linha de um <strong>Recordset</strong>, ou um diretório ou arquivo em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7eabe-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eabe-128"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-p102">Representa o conjunto completo de registros de uma tabela base ou os resultados de um comando executado. Sempre que for adequado, o objeto <strong>Recordset</strong> fará referência somente a um único registro do conjunto como o registro atual.</span><span class="sxs-lookup"><span data-stu-id="7eabe-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eabe-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="7eabe-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="7eabe-132">Representa um fluxo de dados binário.</span><span class="sxs-lookup"><span data-stu-id="7eabe-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

