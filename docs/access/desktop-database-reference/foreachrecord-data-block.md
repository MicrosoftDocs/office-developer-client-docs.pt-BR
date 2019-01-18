---
title: Bloco de dados ParaCadaRegistro
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706342"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="32ffe-102">Bloco de dados ParaCadaRegistro</span><span class="sxs-lookup"><span data-stu-id="32ffe-102">ForEachRecord data block</span></span>

<span data-ttu-id="32ffe-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="32ffe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32ffe-104">Um bloco de dados **ParaCadaRegistro** repete um conjunto de instruções para cada registro em um domínio.</span><span class="sxs-lookup"><span data-stu-id="32ffe-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="32ffe-105">[!OBSERVAçãO] O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="32ffe-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="32ffe-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="32ffe-106">Setting</span></span>

<span data-ttu-id="32ffe-107">A ação **ParaCadaRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="32ffe-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32ffe-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="32ffe-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="32ffe-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32ffe-109">Required</span></span></p></th>
<th><p><span data-ttu-id="32ffe-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="32ffe-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32ffe-111"><strong>Em</strong></span><span class="sxs-lookup"><span data-stu-id="32ffe-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="32ffe-112">Sim</span><span class="sxs-lookup"><span data-stu-id="32ffe-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="32ffe-113">Uma cadeia de caracteres que identifica o domínio de registros para operar em.</span><span class="sxs-lookup"><span data-stu-id="32ffe-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="32ffe-114">O argumento <em>em</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="32ffe-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="32ffe-115"><strong>Observação</strong>: O domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="32ffe-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32ffe-116"><strong>Condição Where</strong></span><span class="sxs-lookup"><span data-stu-id="32ffe-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="32ffe-117">Não</span><span class="sxs-lookup"><span data-stu-id="32ffe-117">No</span></span></p></td>
<td><p><span data-ttu-id="32ffe-118">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>ParaCadaRegistro</strong> é executada.</span><span class="sxs-lookup"><span data-stu-id="32ffe-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="32ffe-119">Por exemplo, critérios costuma ser equivalente à cláusula WHERE em uma expressão SQL, sem a palavra onde.</span><span class="sxs-lookup"><span data-stu-id="32ffe-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="32ffe-120">Se os critérios for omitido, o bloco de dados <strong>ParaCadaRegistro</strong> opera em todo o domínio especificado pelo argumento <em>em</em> .</span><span class="sxs-lookup"><span data-stu-id="32ffe-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="32ffe-121">Qualquer campo que está incluído nos critérios também deve ser um campo no <em>In</em>.</span><span class="sxs-lookup"><span data-stu-id="32ffe-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32ffe-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="32ffe-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="32ffe-123">Não</span><span class="sxs-lookup"><span data-stu-id="32ffe-123">No</span></span></p></td>
<td><p><span data-ttu-id="32ffe-124">Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo argumento <em>em</em> .</span><span class="sxs-lookup"><span data-stu-id="32ffe-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="32ffe-125">Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas. Se o <em>Alias</em> não for especificado, o nome da tabela ou consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="32ffe-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="32ffe-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="32ffe-126">Remarks</span></span>

<span data-ttu-id="32ffe-127">Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente.</span><span class="sxs-lookup"><span data-stu-id="32ffe-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

