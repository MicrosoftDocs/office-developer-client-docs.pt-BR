---
title: Método Recordset2.FindPrevious (DAO)
TOCTitle: FindPrevious Method
ms:assetid: ec35faf4-20f2-a83f-54e4-ac1f66c3c2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836294(v=office.15)
ms:contentKeyID: 48548509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f607025463545d31a49ce116a7e9ddf0cb90270
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463212"
---
# <a name="recordset2findprevious-method-dao"></a><span data-ttu-id="b7b30-102">Método Recordset2.FindPrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7b30-102">Recordset2.FindPrevious Method (DAO)</span></span>


<span data-ttu-id="b7b30-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7b30-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b7b30-p101">Localiza o registro anterior em um objeto **[Recordset](recordset-object-dao.md)** tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="b7b30-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b30-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7b30-106">Syntax</span></span>

<span data-ttu-id="b7b30-107">*expressão* . FindPrevious (***critérios***)</span><span class="sxs-lookup"><span data-stu-id="b7b30-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="b7b30-108">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b7b30-108">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b7b30-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7b30-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7b30-110">Nome</span><span class="sxs-lookup"><span data-stu-id="b7b30-110">Name</span></span></p></th>
<th><p><span data-ttu-id="b7b30-111">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="b7b30-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b7b30-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b7b30-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b7b30-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b30-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-114">Criteria</span><span class="sxs-lookup"><span data-stu-id="b7b30-114">Criteria</span></span></p></td>
<td><p><span data-ttu-id="b7b30-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b7b30-115">Required</span></span></p></td>
<td><p><span data-ttu-id="b7b30-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="b7b30-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b7b30-p102">Uma sequência usada para localizar o registro. Ela é como a cláusula WHERE em uma instrução SQL, mas sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p102">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b7b30-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7b30-119">Remarks</span></span>

<span data-ttu-id="b7b30-p103">Se desejar incluir todos os registros em sua pesquisa, além dos que atendem às condições específicas, use os métodos **Move** para se mover entre registros. Para localizar um registro em um **Conjunto de registros** de tipo tabela, use o método **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p103">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="b7b30-p104">Se a correspondência de critérios do registro não for localizada, o indicador do registro atual será desconhecido e a propriedade **Nenhuma correspondência** será definida como **Verdadeiro**. Se o conjunto de registros incluir mais de um registro que satisfaça os critérios, o **FindFirst** vai localizar a primeira ocorrência, o **FindNext** vai localizar a próxima ocorrência, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p104">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="b7b30-124">Todos os métodos **Find** iniciam suas pesquisas a partir do local e na direção especificada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7b30-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7b30-125">Método Find</span><span class="sxs-lookup"><span data-stu-id="b7b30-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="b7b30-126">Inicia pesquisa em</span><span class="sxs-lookup"><span data-stu-id="b7b30-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="b7b30-127">Direção da pesquisa</span><span class="sxs-lookup"><span data-stu-id="b7b30-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="b7b30-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="b7b30-129">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b7b30-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="b7b30-130">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b7b30-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="b7b30-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="b7b30-132">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b7b30-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="b7b30-133">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b7b30-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="b7b30-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="b7b30-135">Registro atual</span><span class="sxs-lookup"><span data-stu-id="b7b30-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="b7b30-136">Fim do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b7b30-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="b7b30-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="b7b30-138">Registro atual</span><span class="sxs-lookup"><span data-stu-id="b7b30-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="b7b30-139">Início do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b7b30-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b7b30-p105">No entanto, utilizar um dos métodos **Find** não é o mesmo que utilizar um método **Move**, que simplesmente torna atual o primeiro, o último, o anterior ou o próximo registro sem especificar uma condição. A operação Find pode ser seguida pela operação Move.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p105">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="b7b30-p106">Sempre verifique o valor da propriedade **NoMatch** para determinar se a operação Find foi bem-sucedida. Se a pesquisa for bem-sucedida, **NoMatch** será **False**. Se ela falhar, **NoMatch** será **True**, e o registro atual não será definido. Nesse caso, você deve posicionar o ponteiro atual do registro de volta em um registro válido.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p106">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="b7b30-p107">Utilizar o método **Find** com os conjuntos de registros com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access pode não ser eficaz. Você poderá constatar que reformular os critérios para localizar um registro específico seja mais rápido, especialmente quando se trabalha com grandes conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p107">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="b7b30-p108">Ao trabalhar com os bancos de dados com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access e por grande objetos tipo dynaset do **Conjunto de registros**, você poderá descobrir que usar os métodos **Find** ou as propriedades **Classificar** ou **Filtrar** é mais lento. Para melhorar o desempenho, use as consultas SQL cláusulas ORDER BY ou WHERE, consultas de parâmetro ou objetos **QueryDef** personalizados, que recuperam registros específicos indexados.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="b7b30-p109">Você deve usar o formato de data americano (mês-dia-ano) ao pesquisar campos contendo datas, mesmo que não esteja utilizando uma versão em inglês do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados não poderão ser localizado. Use a função **Format** do Visual Basic para converter a data. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b7b30-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="b7b30-153">Se os critérios é composta por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Chame o método.</span><span class="sxs-lookup"><span data-stu-id="b7b30-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="b7b30-154">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b7b30-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="b7b30-155">Para melhor desempenho, os <EM>critérios</EM> devem estar em um formato "<EM>campo</EM> = <EM>valor</EM>" onde o <EM>campo</EM> é um campo indexado na tabela base ou "<EM>campo</EM> como <EM>prefixo</EM>" onde o <EM>campo</EM> é um campo indexado na tabela base e <EM>prefixo</EM> é uma cadeia de caracteres de pesquisa do prefixo (por exemplo, "ART \*").</span><span class="sxs-lookup"><span data-stu-id="b7b30-155">For best performance, the <EM>criteria</EM> should be in either the form "<EM>field</EM> = <EM>value</EM>" where <EM>field</EM> is an indexed field in the underlying base table, or "<EM>field</EM> LIKE <EM>prefix</EM>" where <EM>field</EM> is an indexed field in the underlying base table and <EM>prefix</EM> is a prefix search string (for example, "ART\*" ).</span></span></P>
> <LI>
> <P><span data-ttu-id="b7b30-p111">Em geral, para tipos equivalentes de pesquisa, o método <STRONG>Seek</STRONG> fornece melhor desempenho que os métodos <STRONG>Find</STRONG>. Isso significa que os objetos <STRONG>Recordset</STRONG> tipo tabela sozinhos podem atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="b7b30-p111">In general, for equivalent types of searches, the <STRONG>Seek</STRONG> method provides better performance than the <STRONG>Find</STRONG> methods. This assumes that table-type <STRONG>Recordset</STRONG> objects alone can satisfy your needs.</span></span></P></LI></UL>


