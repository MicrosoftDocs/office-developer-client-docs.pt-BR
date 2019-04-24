---
title: Método Recordset. FindLast (DAO)
TOCTitle: FindLast Method
ms:assetid: 65236519-3474-a760-99bc-2e8f6bfeee7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195128(v=office.15)
ms:contentKeyID: 48545311
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 306f817779c47b48843df0fb51a023002ed88bf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300949"
---
# <a name="recordsetfindlast-method-dao"></a><span data-ttu-id="652d9-102">Método Recordset. FindLast (DAO)</span><span class="sxs-lookup"><span data-stu-id="652d9-102">Recordset.FindLast method (DAO)</span></span>

<span data-ttu-id="652d9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="652d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="652d9-104">Localiza o último registro em um objeto **[Recordset](recordset-object-dao.md)** tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (Apenas Espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="652d9-104">Locates the last record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="652d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="652d9-105">Syntax</span></span>

<span data-ttu-id="652d9-106">*expressão* . FindLast (***critérios***)</span><span class="sxs-lookup"><span data-stu-id="652d9-106">*expression* .FindLast(***Criteria***)</span></span>

<span data-ttu-id="652d9-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="652d9-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="652d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="652d9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="652d9-109">Nome</span><span class="sxs-lookup"><span data-stu-id="652d9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="652d9-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="652d9-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="652d9-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="652d9-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="652d9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="652d9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="652d9-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="652d9-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="652d9-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="652d9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="652d9-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="652d9-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="652d9-116">Uma sequência usada para localizar o registro.</span><span class="sxs-lookup"><span data-stu-id="652d9-116">A String used to locate the record.</span></span> <span data-ttu-id="652d9-117">Ela é como a cláusula WHERE em uma instrução SQL, mas sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="652d9-117">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="652d9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="652d9-118">Remarks</span></span>

<span data-ttu-id="652d9-p102">Se desejar incluir todos os registros em sua pesquisa, além dos que atendem às condições específicas, use os métodos **Move** para se mover entre registros. Para localizar um registro em um **Conjunto de registros** de tipo tabela, use o método **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="652d9-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="652d9-p103">Se a correspondência de critérios do registro não for localizada, o indicador do registro atual será desconhecido e a propriedade **Nenhuma correspondência** será definida como **Verdadeiro**. Se o conjunto de registros incluir mais de um registro que satisfaça os critérios, o **FindFirst** vai localizar a primeira ocorrência, o **FindNext** vai localizar a próxima ocorrência, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="652d9-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="652d9-123">Todos os métodos **Find** iniciam suas pesquisas a partir do local e na direção especificada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="652d9-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="652d9-124">Método Find</span><span class="sxs-lookup"><span data-stu-id="652d9-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="652d9-125">Começa a pesquisa em</span><span class="sxs-lookup"><span data-stu-id="652d9-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="652d9-126">Direção de pesquisa</span><span class="sxs-lookup"><span data-stu-id="652d9-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="652d9-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="652d9-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="652d9-128">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="652d9-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="652d9-129">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="652d9-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="652d9-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="652d9-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="652d9-131">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="652d9-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="652d9-132">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="652d9-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="652d9-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="652d9-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="652d9-134">Registro atual</span><span class="sxs-lookup"><span data-stu-id="652d9-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="652d9-135">Final do recordset</span><span class="sxs-lookup"><span data-stu-id="652d9-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="652d9-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="652d9-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="652d9-137">Registro atual</span><span class="sxs-lookup"><span data-stu-id="652d9-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="652d9-138">Início do recordset</span><span class="sxs-lookup"><span data-stu-id="652d9-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="652d9-139">Quando você usa o método **FindLast**, o mecanismo de banco de dados do Microsoft Access preenche totalmente seu **Recordset** antes do início da pesquisa, se isso ainda não aconteceu.</span><span class="sxs-lookup"><span data-stu-id="652d9-139">When you use the **FindLast** method, the Microsoft Access database engine fully populates your **Recordset** before beginning the search, if this hasn't already happened.</span></span>

<span data-ttu-id="652d9-p104">No entanto, utilizar um dos métodos **Find** não é o mesmo que utilizar um método **Move**, que simplesmente torna atual o primeiro, o último, o anterior ou o próximo registro sem especificar uma condição. A operação Find pode ser seguida pela operação Move.</span><span class="sxs-lookup"><span data-stu-id="652d9-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="652d9-p105">Sempre verifique o valor da propriedade **NoMatch** para determinar se a operação Find foi bem-sucedida. Se a pesquisa for bem-sucedida, **NoMatch** será **False**. Se ela falhar, **NoMatch** será **True**, e o registro atual não será definido. Nesse caso, você deve posicionar o ponteiro atual do registro de volta em um registro válido.</span><span class="sxs-lookup"><span data-stu-id="652d9-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="652d9-p106">Utilizar o método **Find** com os conjuntos de registros com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access pode não ser eficaz. Você poderá constatar que reformular os critérios para localizar um registro específico seja mais rápido, especialmente quando se trabalha com grandes conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="652d9-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="652d9-p107">Ao trabalhar com os bancos de dados com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access e por grande objetos tipo dynaset do **Conjunto de registros**, você poderá descobrir que usar os métodos **Find** ou as propriedades **Classificar** ou **Filtrar** é mais lento. Para melhorar o desempenho, use as consultas SQL cláusulas ORDER BY ou WHERE, consultas de parâmetro ou objetos **QueryDef** personalizados, que recuperam registros específicos indexados.</span><span class="sxs-lookup"><span data-stu-id="652d9-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="652d9-p108">Você deve usar o formato de data americano (mês-dia-ano) ao pesquisar campos contendo datas, mesmo que não esteja utilizando uma versão em inglês do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados não poderão ser localizado. Use a função **Format** do Visual Basic para converter a data. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="652d9-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="652d9-153">Se os critérios forem compostos de uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere não-U. decimal, como vírgula (por exemplo, strSQL = "PRICE \> " & lngPrice e lngPrice = 125, 50), ocorrerá um erro quando você tentar chamar o método.</span><span class="sxs-lookup"><span data-stu-id="652d9-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="652d9-154">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="652d9-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="652d9-155">Para obter um melhor desempenho, os *critérios* devem estar no formato "\*\* = *valor*do campo" onde *campo* é um campo indexado na tabela base subjacente ou "*campo* como *prefixo*" onde *campo* é um campo indexado na tabela base subjacente e o *prefixo* é uma cadeia de caracteres de pesquisa de prefixo (por exemplo, "Art \*").</span><span class="sxs-lookup"><span data-stu-id="652d9-155">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="652d9-p110">Em geral, para tipos equivalentes de pesquisa, o método **Seek** fornece melhor desempenho que os métodos **Find**. Isso significa que os objetos **Recordset** tipo tabela sozinhos podem atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="652d9-p110">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


