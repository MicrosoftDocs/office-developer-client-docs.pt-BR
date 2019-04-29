---
title: Método Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300634"
---
# <a name="recordsetfindnext-method-dao"></a><span data-ttu-id="bfa92-102">Método Recordset.FindNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="bfa92-102">Recordset.FindNext method (DAO)</span></span>

<span data-ttu-id="bfa92-103">**Aplica-se a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfa92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfa92-104">Localiza o próximo registro em um objeto **[Recordset](recordset-object-dao.md)** tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="bfa92-104">Locates the next record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfa92-105">Syntax</span></span>

<span data-ttu-id="bfa92-106">*expression* .FindNext(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="bfa92-106">*expression* .FindNext(***Criteria***)</span></span>

<span data-ttu-id="bfa92-107">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bfa92-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="bfa92-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfa92-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfa92-109">Nome</span><span class="sxs-lookup"><span data-stu-id="bfa92-109">Name</span></span></p></th>
<th><p><span data-ttu-id="bfa92-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="bfa92-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="bfa92-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bfa92-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="bfa92-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfa92-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfa92-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="bfa92-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="bfa92-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bfa92-114">Required</span></span></p></td>
<td><p><span data-ttu-id="bfa92-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="bfa92-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="bfa92-116">Uma sequência usada para localizar o registro.</span><span class="sxs-lookup"><span data-stu-id="bfa92-116">A String used to locate the record.</span></span> <span data-ttu-id="bfa92-117">Ela é como a cláusula WHERE em uma instrução SQL, mas sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="bfa92-117">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bfa92-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfa92-118">Remarks</span></span>

<span data-ttu-id="bfa92-p102">Se desejar incluir todos os registros em sua pesquisa, além dos que atendem às condições específicas, use os métodos **Move** para se mover entre registros. Para localizar um registro em um **Conjunto de registros** de tipo tabela, use o método **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="bfa92-p103">Se a correspondência de critérios do registro não for localizada, o indicador do registro atual será desconhecido e a propriedade **Nenhuma correspondência** será definida como **Verdadeiro**. Se o conjunto de registros incluir mais de um registro que satisfaça os critérios, o **FindFirst** vai localizar a primeira ocorrência, o **FindNext** vai localizar a próxima ocorrência, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="bfa92-123">Todos os métodos **Find** iniciam suas pesquisas a partir do local e na direção especificada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfa92-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfa92-124">Método Find</span><span class="sxs-lookup"><span data-stu-id="bfa92-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="bfa92-125">Inicia pesquisa em</span><span class="sxs-lookup"><span data-stu-id="bfa92-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="bfa92-126">Direção da pesquisa</span><span class="sxs-lookup"><span data-stu-id="bfa92-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfa92-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="bfa92-127"><strong>FindFirst method</strong></span></span></p></td>
<td><p><span data-ttu-id="bfa92-128">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="bfa92-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="bfa92-129">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="bfa92-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfa92-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="bfa92-130"><strong>FindLast method</strong></span></span></p></td>
<td><p><span data-ttu-id="bfa92-131">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="bfa92-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="bfa92-132">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="bfa92-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfa92-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="bfa92-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="bfa92-134">Registro atual</span><span class="sxs-lookup"><span data-stu-id="bfa92-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="bfa92-135">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="bfa92-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfa92-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="bfa92-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="bfa92-137">Registro atual</span><span class="sxs-lookup"><span data-stu-id="bfa92-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="bfa92-138">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="bfa92-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bfa92-p104">No entanto, utilizar um dos métodos **Find** não é o mesmo que utilizar um método **Move**, que simplesmente torna atual o primeiro, o último, o anterior ou o próximo registro sem especificar uma condição. A operação Find pode ser seguida pela operação Move.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="bfa92-p105">Sempre verifique o valor da propriedade **NoMatch** para determinar se a operação Find foi bem-sucedida. Se a pesquisa for bem-sucedida, **NoMatch** será **False**. Se ela falhar, **NoMatch** será **True**, e o registro atual não será definido. Nesse caso, você deve posicionar o ponteiro atual do registro de volta em um registro válido.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="bfa92-p106">Utilizar o método **Find** com os conjuntos de registros com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access pode não ser eficaz. Você poderá constatar que reformular os critérios para localizar um registro específico seja mais rápido, especialmente quando se trabalha com grandes conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="bfa92-147">Em um espaço de trabalho ODBCDirect, os métodos **Find** e **Seek** não estão disponíveis em nenhum tipo de objeto **Recordset**, porque executar um método **Find** ou **Seek** por meio de uma conexão ODBC não é muito eficiente na rede.</span><span class="sxs-lookup"><span data-stu-id="bfa92-147">In an ODBCDirect workspace, the **Find** and **Seek** methods are not available on any type of **Recordset** object, because executing a **Find** or **Seek** through an ODBC connection is not very efficient over the network.</span></span> <span data-ttu-id="bfa92-148">Em vez disso, você deve projetar a consulta (isto é, utilizando o argumento source para o método **OpenRecordset**) com uma cláusula WHERE apropriada que restrinja os registros retornados a apenas aqueles que corresponderem aos critérios utilizados em um método **Find** ou **Seek**.</span><span class="sxs-lookup"><span data-stu-id="bfa92-148">Instead, you should design the query (that is, using the  source argument to the **OpenRecordset** method) with an appropriate WHERE clause that restricts the returned records to only those that meet the criteria you would otherwise use in a **Find** or **Seek** method.</span></span>

<span data-ttu-id="bfa92-p108">Ao trabalhar com bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access e com grandes objetos v tipo dynaset, você poderá descobrir que a utilização dos métodos **Find** ou da propriedade **Sort** ou **Filter** é lenta. Para aprimorar o desempenho, use as consultas SQL com cláusulas ORDER BY ou WHERE personalizadas, consultas de parâmetro ou objetos **QueryDef** que recuperam registros específicos e indexados.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type v objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="bfa92-p109">É necessário usar o formato de data dos EUA (mês/dia/ano), ao pesquisar campos contendo datas, mesmo se não estiver usando a versão norte-americana do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados podem não ser encontrados. Use a função **Formato** do Visual Basic para converter a data. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="bfa92-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="bfa92-154">Se o critério for composto por uma cadeia concatenada de caracteres e com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), ocorrerá um erro ao tentar chamar o método.</span><span class="sxs-lookup"><span data-stu-id="bfa92-154">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="bfa92-155">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="bfa92-155">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="bfa92-156">Para melhorar o desempenho, *criteria* deve estar no formato "*field* = *value*", no qual *field* é um campo indexado na tabela base, ou no formato "*field* LIKE *prefix*", no qual *field* é um campo indexado na tabela base e *prefix* é uma sequência de pesquisa de prefixo (por exemplo, "ART\*").</span><span class="sxs-lookup"><span data-stu-id="bfa92-156">For best performance, the criteria should be in either the form "field = value" where field is an indexed field in the underlying base table, or "field LIKE prefix" where field is an indexed field in the underlying base table and prefix is a prefix search string (for example, "ART\*"
).</span></span>
> 
> - <span data-ttu-id="bfa92-p111">De modo geral, para os tipos de pesquisas, o método **Seek** proporciona um melhor desempenho do que o método **Find**. Isso supõe que os objetos de tipo de tabela **Conjunto de registros** sozinhos podem atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="bfa92-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="bfa92-159">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bfa92-159">Example</span></span>

<span data-ttu-id="bfa92-160">O exemplo a seguir mostra como usar os métodos FindFirst e FindNext para localizar um registro em um Conjunto de Registros.</span><span class="sxs-lookup"><span data-stu-id="bfa92-160">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="bfa92-161">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bfa92-161">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
