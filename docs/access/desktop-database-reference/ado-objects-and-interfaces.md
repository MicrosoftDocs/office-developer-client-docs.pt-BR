---
title: Objetos e Interfaces do ADO
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efab7ce2980393282ee1f96295206e712fcbd15f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882179"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="f7582-102">Objetos e Interfaces do ADO</span><span class="sxs-lookup"><span data-stu-id="f7582-102">ADO Objects and Interfaces</span></span>


<span data-ttu-id="f7582-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7582-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7582-104">As relações entre esses objetos são representadas no Modelo de objeto do ADOX.</span><span class="sxs-lookup"><span data-stu-id="f7582-104">The relationships between these objects are represented in the ADO Object Model.</span></span>

<span data-ttu-id="f7582-p101">Cada objeto pode estar contido em sua coleção correspondente. Por exemplo, um objeto [Error](error-object-ado.md) pode estar contido em uma coleção [Errors](errors-collection-ado.md). Para obter mais informações, consulte [Coleções do ADO](ado-collections.md) ou um tópico de coleção específico.</span><span class="sxs-lookup"><span data-stu-id="f7582-p101">Each object can be contained in its corresponding collection. For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection. For more information, see [ADO Collections](ado-collections.md) or a specific collection topic.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7582-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="f7582-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-109">Constrói um objeto <strong>Record</strong> do ADO a partir de um objeto <strong>Row</strong> do OLE DB em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="f7582-109">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7582-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="f7582-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-111">Constrói um objeto <strong>Recordset</strong> do ADO a partir de um objeto <strong>Rowset</strong> do OLE DB em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="f7582-111">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7582-112"><a href="error-object-ado.md">Erro</a></span><span class="sxs-lookup"><span data-stu-id="f7582-112"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-113">Contém os detalhes sobre os erros de acesso aos dados que pertencem à uma única operação que envolve o provedor.</span><span class="sxs-lookup"><span data-stu-id="f7582-113">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7582-114"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="f7582-114"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-115">Representa uma coluna de dados com um tipo de dados comuns.</span><span class="sxs-lookup"><span data-stu-id="f7582-115">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7582-116"><a href="parameter-object-ado.md">Parâmetro</a></span><span class="sxs-lookup"><span data-stu-id="f7582-116"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-117">Representa um parâmetro ou argumento associado ao objeto <strong>Command</strong> com base em uma consulta parametrizada ou em um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="f7582-117">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7582-118"><a href="property-object-ado.md">Propriedade</a></span><span class="sxs-lookup"><span data-stu-id="f7582-118"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-119">Representa uma característica dinâmica de um objeto ADO definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="f7582-119">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7582-120"><a href="record-object-ado.md">Objeto Record</a></span><span class="sxs-lookup"><span data-stu-id="f7582-120"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-121">Representa uma linha de um <strong>Recordset</strong>, ou um diretório ou arquivo em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f7582-121">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7582-122"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="f7582-122"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-p102">Representa o conjunto completo de registros de uma tabela base ou os resultados de um comando executado. Sempre que for adequado, o objeto <strong>Recordset</strong> fará referência somente a um único registro do conjunto como o registro atual.</span><span class="sxs-lookup"><span data-stu-id="f7582-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7582-125"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="f7582-125"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="f7582-126">Representa um fluxo de dados binário.</span><span class="sxs-lookup"><span data-stu-id="f7582-126">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

