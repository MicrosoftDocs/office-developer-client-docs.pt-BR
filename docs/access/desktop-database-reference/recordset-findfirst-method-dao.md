---
title: Método Recordset.FindFirst (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23f7609cb918ce1dc04c17d84178daf2ce43be31
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925391"
---
# <a name="recordsetfindfirst-method-dao"></a><span data-ttu-id="4ca7d-102">Método Recordset.FindFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ca7d-102">Recordset.FindFirst method (DAO)</span></span>

<span data-ttu-id="4ca7d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ca7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ca7d-104">Localiza o primeiro registro em um dynaset ou objeto de tipo instantâneo do **Conjunto de registros**, que atende aos critérios específicos e torna esse registro atual (somente para espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4ca7d-104">Locates the first record in a dynaset- or snapshot-type **Recordset** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ca7d-105">Syntax</span></span>

<span data-ttu-id="4ca7d-106">*expressão* . FindFirst (***critérios***)</span><span class="sxs-lookup"><span data-stu-id="4ca7d-106">*expression* .FindFirst(***Criteria***)</span></span>

<span data-ttu-id="4ca7d-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="4ca7d-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="4ca7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca7d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="4ca7d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4ca7d-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="4ca7d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="4ca7d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4ca7d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="4ca7d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ca7d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca7d-113">Criteria</span><span class="sxs-lookup"><span data-stu-id="4ca7d-113">Criteria</span></span></p></td>
<td><p><span data-ttu-id="4ca7d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ca7d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4ca7d-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="4ca7d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="4ca7d-p101">Uma sequência usada para localizar o registro. Ela é como a cláusula WHERE em uma instrução SQL, mas sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4ca7d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca7d-118">Remarks</span></span>

<span data-ttu-id="4ca7d-p102">Se desejar incluir todos os registros em sua pesquisa, além dos que atendem às condições específicas, use os métodos **Move** para se mover entre registros. Para localizar um registro em um **Conjunto de registros** de tipo tabela, use o método **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="4ca7d-p103">Se a correspondência de critérios do registro não for localizada, o indicador do registro atual será desconhecido e a propriedade **Nenhuma correspondência** será definida como **Verdadeiro**. Se o conjunto de registros incluir mais de um registro que satisfaça os critérios, o **FindFirst** vai localizar a primeira ocorrência, o **FindNext** vai localizar a próxima ocorrência, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="4ca7d-123">Todos os métodos **Find** iniciam suas pesquisas a partir do local e na direção especificada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca7d-124">Método Find</span><span class="sxs-lookup"><span data-stu-id="4ca7d-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="4ca7d-125">Inicia pesquisa em</span><span class="sxs-lookup"><span data-stu-id="4ca7d-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="4ca7d-126">Direção da pesquisa</span><span class="sxs-lookup"><span data-stu-id="4ca7d-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca7d-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="4ca7d-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="4ca7d-128">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="4ca7d-129">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca7d-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="4ca7d-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="4ca7d-131">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="4ca7d-132">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ca7d-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="4ca7d-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="4ca7d-134">Registro atual</span><span class="sxs-lookup"><span data-stu-id="4ca7d-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="4ca7d-135">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca7d-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="4ca7d-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="4ca7d-137">Registro atual</span><span class="sxs-lookup"><span data-stu-id="4ca7d-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="4ca7d-138">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ca7d-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ca7d-p104">No entanto, utilizar um dos métodos **Find** não é o mesmo que utilizar um método **Move**, que simplesmente torna atual o primeiro, o último, o anterior ou o próximo registro sem especificar uma condição. A operação Find pode ser seguida pela operação Move.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="4ca7d-p105">Sempre verifique o valor da propriedade **NoMatch** para determinar se a operação Find foi bem-sucedida. Se a pesquisa for bem-sucedida, **NoMatch** será **False**. Se ela falhar, **NoMatch** será **True**, e o registro atual não será definido. Nesse caso, você deve posicionar o ponteiro atual do registro de volta em um registro válido.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="4ca7d-p106">Utilizar o método **Find** com os conjuntos de registros com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access pode não ser eficaz. Você poderá constatar que reformular os critérios para localizar um registro específico seja mais rápido, especialmente quando se trabalha com grandes conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="4ca7d-p107">Ao trabalhar com os bancos de dados com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access e por grande objetos tipo dynaset do **Conjunto de registros**, você poderá descobrir que usar os métodos **Find** ou as propriedades **Classificar** ou **Filtrar** é mais lento. Para melhorar o desempenho, use as consultas SQL cláusulas ORDER BY ou WHERE, consultas de parâmetro ou objetos **QueryDef** personalizados, que recuperam registros específicos indexados.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="4ca7d-p108">Você deve usar o formato de data americano (mês-dia-ano) ao pesquisar campos contendo datas, mesmo que não esteja utilizando uma versão em inglês do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados não poderão ser localizado. Use a função **Format** do Visual Basic para converter a data. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="4ca7d-152">Se os critérios é composta por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Chame o método.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-152">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="4ca7d-153">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-153">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> - <span data-ttu-id="4ca7d-154">Para melhor desempenho, os *critérios* devem estar em um formato "*campo* = *valor*" onde o *campo* é um campo indexado na tabela base ou "*campo* como *prefixo*" onde o *campo* é um campo indexado na tabela base e *prefixo* é uma cadeia de caracteres de pesquisa do prefixo (por exemplo, "ART \*").</span><span class="sxs-lookup"><span data-stu-id="4ca7d-154">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*" ).</span></span>
> 
> - <span data-ttu-id="4ca7d-p110">Em geral, para tipos equivalentes de pesquisa, o método **Seek** fornece melhor desempenho que os métodos **Find**. Isso significa que os objetos **Recordset** tipo tabela sozinhos podem atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-p110">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="4ca7d-157">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4ca7d-157">Example</span></span>

<span data-ttu-id="4ca7d-158">O exemplo a seguir mostra como usar os métodos FindFirst e FindNext para localizar um registro em um Recordset.</span><span class="sxs-lookup"><span data-stu-id="4ca7d-158">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="4ca7d-159">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4ca7d-159">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
