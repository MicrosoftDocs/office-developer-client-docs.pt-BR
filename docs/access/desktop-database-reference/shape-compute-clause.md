---
title: Cláusula de cálculo de forma
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711522"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="30279-102">Cláusula de cálculo de forma</span><span class="sxs-lookup"><span data-stu-id="30279-102">Shape Compute clause</span></span>

<span data-ttu-id="30279-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="30279-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30279-104">Uma cláusula COMPUTE de forma gera um **Recordset** pai, cujas colunas consistem em uma referência ao **Recordset** filho; colunas opcionais cujo conteúdo são colunas de capítulo, colunas novas ou colunas calculadas, ou o resultado da execução de funções agregadas no **Recordset** filho ou em um **Recordset** com formato anterior; e todas as colunas do **Recordset** filho listado na cláusula BY opcional.</span><span class="sxs-lookup"><span data-stu-id="30279-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="30279-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30279-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="30279-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="30279-106">Description</span></span>

<span data-ttu-id="30279-107">As partes dessa cláusula são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="30279-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="30279-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="30279-108">*child-command*</span></span>

  - <span data-ttu-id="30279-109">Consiste em um dos itens a seguir:</span><span class="sxs-lookup"><span data-stu-id="30279-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="30279-p101">Um comando de consulta entre chaves ("{}") que retorna um objeto **Recordset** filho. O comando é emitido para o provedor de dados subjacente, e sua sintaxe depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.</span><span class="sxs-lookup"><span data-stu-id="30279-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="30279-113">O nome de um **Recordset** com formato existente.</span><span class="sxs-lookup"><span data-stu-id="30279-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="30279-114">Um outro comando shape.</span><span class="sxs-lookup"><span data-stu-id="30279-114">Another shape command.</span></span>
    
    - <span data-ttu-id="30279-115">A palavra-chave TABLE, seguida do nome de uma tabela no provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="30279-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="30279-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="30279-116">*child-alias*</span></span>

  - <span data-ttu-id="30279-117">Um alias usado para se referir ao **Recordset** retornado pelo *filho-command.*</span><span class="sxs-lookup"><span data-stu-id="30279-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="30279-118">O *alias de filhos* for exigida na lista de colunas na cláusula COMPUTE e define a relação entre os objetos **Recordset** pai e filho.</span><span class="sxs-lookup"><span data-stu-id="30279-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="30279-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="30279-119">*appended-column-list*</span></span>

  - <span data-ttu-id="30279-p103">Uma lista na qual cada elemento define uma coluna no pai gerado. Cada elemento consiste em uma coluna de capítulo, uma nova coluna, uma coluna calculada ou um valor resultante de uma função de agregação no **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="30279-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="30279-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="30279-122">*grp-field-list*</span></span>

  - <span data-ttu-id="30279-123">Uma lista de colunas nos objetos **Recordset** pai e filho que especifica o modo de agrupamento das linhas no filho.</span><span class="sxs-lookup"><span data-stu-id="30279-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="30279-124">Para cada coluna na *grp--lista de campos,* há uma coluna correspondente nos objetos **Recordset** pai e filho.</span><span class="sxs-lookup"><span data-stu-id="30279-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="30279-125">Para cada linha no **Recordset**pai, as colunas de *lista de campos grp* têm valores exclusivos e o filho **Recordset** referenciado da linha pai consiste exclusivamente filho linhas cuja *lista de campos grp* colunas têm os mesmos valores que o linha pai.</span><span class="sxs-lookup"><span data-stu-id="30279-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="30279-p105">Se a cláusula BY for incluída, as linhas do **Recordset** filho serão agrupadas com base nas colunas na cláusula COMPUTE. O **Recordset** pai conterá uma linha para cada grupo de linhas no **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="30279-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="30279-p106">Se a cláusula BY for omitida, todo o **Recordset** filho será tratado como um único grupo e o **Recordset** pai conterá exatamente uma linha. Essa linha fará referência a todo o **Recordset** filho. A omissão da cláusula BY permite calcular o "total geral" de agregados em todo o **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="30279-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="30279-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="30279-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="30279-p107">Independentemente do modo de formação do **Recordset** pai (usando COMPUTE ou APPEND), ele conterá uma coluna de capítulo usada para relacioná-lo a um **Recordset** filho. Se você desejar, o **Recordset** pai também poderá conter colunas com agregados (SUM, MIN, MAX etc.) nas linhas filho. Os objetos **Recordset** pai e filho podem conter colunas com uma expressão na linha de **Recordset**, bem como colunas novas e inicialmente vazias.</span><span class="sxs-lookup"><span data-stu-id="30279-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="30279-135">Operação</span><span class="sxs-lookup"><span data-stu-id="30279-135">Operation</span></span>

<span data-ttu-id="30279-136">O *comando filho* é emitida para o provedor, que retorna um **Recordset**filho.</span><span class="sxs-lookup"><span data-stu-id="30279-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="30279-p108">A cláusula COMPUTE especifica as colunas do **Recordset** pai, que pode ser uma referência ao **Recordset** filho, um ou mais agregados, uma expressão calculada ou novas colunas. Se houver uma cláusula BY, as colunas definidas por ela também serão acrescentadas ao **Recordset** pai. A cláusula BY especifica o modo de agrupamento do **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="30279-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="30279-140">Por exemplo, suponha que você tenha uma tabela  Demografia  contendo os campos Estado, Cidade e População (os números referentes à população são apenas para fins ilustrativos).</span><span class="sxs-lookup"><span data-stu-id="30279-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30279-141">Estado</span><span class="sxs-lookup"><span data-stu-id="30279-141">State</span></span></p></th>
<th><p><span data-ttu-id="30279-142">Cidade</span><span class="sxs-lookup"><span data-stu-id="30279-142">City</span></span></p></th>
<th><p><span data-ttu-id="30279-143">População</span><span class="sxs-lookup"><span data-stu-id="30279-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30279-144">WA</span><span class="sxs-lookup"><span data-stu-id="30279-144">WA</span></span></p></td>
<td><p><span data-ttu-id="30279-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="30279-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="30279-146">700.000</span><span class="sxs-lookup"><span data-stu-id="30279-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-147">OR</span><span class="sxs-lookup"><span data-stu-id="30279-147">OR</span></span></p></td>
<td><p><span data-ttu-id="30279-148">Medford</span><span class="sxs-lookup"><span data-stu-id="30279-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="30279-149">200.000</span><span class="sxs-lookup"><span data-stu-id="30279-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30279-150">OR</span><span class="sxs-lookup"><span data-stu-id="30279-150">OR</span></span></p></td>
<td><p><span data-ttu-id="30279-151">Portland</span><span class="sxs-lookup"><span data-stu-id="30279-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="30279-152">400.000</span><span class="sxs-lookup"><span data-stu-id="30279-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-153">CA</span><span class="sxs-lookup"><span data-stu-id="30279-153">CA</span></span></p></td>
<td><p><span data-ttu-id="30279-154">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="30279-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="30279-155">800.000</span><span class="sxs-lookup"><span data-stu-id="30279-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30279-156">CA</span><span class="sxs-lookup"><span data-stu-id="30279-156">CA</span></span></p></td>
<td><p><span data-ttu-id="30279-157">San Diego</span><span class="sxs-lookup"><span data-stu-id="30279-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="30279-158">600.000</span><span class="sxs-lookup"><span data-stu-id="30279-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-159">WA</span><span class="sxs-lookup"><span data-stu-id="30279-159">WA</span></span></p></td>
<td><p><span data-ttu-id="30279-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="30279-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="30279-161">500.000</span><span class="sxs-lookup"><span data-stu-id="30279-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30279-162">OR</span><span class="sxs-lookup"><span data-stu-id="30279-162">OR</span></span></p></td>
<td><p><span data-ttu-id="30279-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="30279-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="30279-164">300.000</span><span class="sxs-lookup"><span data-stu-id="30279-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30279-165">Agora, emita este comando shape:</span><span class="sxs-lookup"><span data-stu-id="30279-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="30279-166">O comando abre um **Recordset** com formato de dois níveis.</span><span class="sxs-lookup"><span data-stu-id="30279-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="30279-167">O nível do pai é um **conjunto de registros** de gerado com uma coluna agregada (SUM(rs.population)), uma coluna que faz referência a **Recordset** (rs) filho e uma coluna para agrupamento do **Recordset** (estado) filho.</span><span class="sxs-lookup"><span data-stu-id="30279-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="30279-168">Nível filho é o **conjunto de registros** retornado por uma coluna para agrupamento do **Recordset** (estado) filho, uma coluna que faz referência a **Recordset** (rs) filho e o comando de consulta ().</span><span class="sxs-lookup"><span data-stu-id="30279-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="30279-169">Nível filho é o **conjunto de registros** retornados pelo comando consulta (selecione \* de demografia).</span><span class="sxs-lookup"><span data-stu-id="30279-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="30279-p110">As linhas de detalhes do **Recordset** filho serão agrupadas por estado, mas sem nenhuma ordem específica, ou seja, os grupos não estarão em ordem alfabética ou numérica. Se desejar ordenar o **Recordset** pai, você poderá usar o método **Sort** de **Recordset** para ordenar o **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="30279-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="30279-p111">Agora, você pode navegar pelo **Recordset** pai aberto e acessar os objetos **Recordset** filho de detalhes. Para obter mais informações, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="30279-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="30279-175">**Conjuntos de registros de detalhes pai e filho resultantes**</span><span class="sxs-lookup"><span data-stu-id="30279-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="30279-176">**Pai**</span><span class="sxs-lookup"><span data-stu-id="30279-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30279-177">SUM (rs.Population)</span><span class="sxs-lookup"><span data-stu-id="30279-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="30279-178">rs</span><span class="sxs-lookup"><span data-stu-id="30279-178">rs</span></span></p></th>
<th><p><span data-ttu-id="30279-179">State</span><span class="sxs-lookup"><span data-stu-id="30279-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30279-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="30279-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="30279-181">Referência ao filho1</span><span class="sxs-lookup"><span data-stu-id="30279-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="30279-182">CA</span><span class="sxs-lookup"><span data-stu-id="30279-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="30279-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="30279-184">Referência ao filho2</span><span class="sxs-lookup"><span data-stu-id="30279-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="30279-185">WA</span><span class="sxs-lookup"><span data-stu-id="30279-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30279-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="30279-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="30279-187">Referência ao filho3</span><span class="sxs-lookup"><span data-stu-id="30279-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="30279-188">OR</span><span class="sxs-lookup"><span data-stu-id="30279-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30279-189">**Filho1**</span><span class="sxs-lookup"><span data-stu-id="30279-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30279-190">Estado</span><span class="sxs-lookup"><span data-stu-id="30279-190">State</span></span></p></th>
<th><p><span data-ttu-id="30279-191">Cidade</span><span class="sxs-lookup"><span data-stu-id="30279-191">City</span></span></p></th>
<th><p><span data-ttu-id="30279-192">População</span><span class="sxs-lookup"><span data-stu-id="30279-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30279-193">CA</span><span class="sxs-lookup"><span data-stu-id="30279-193">CA</span></span></p></td>
<td><p><span data-ttu-id="30279-194">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="30279-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="30279-195">800.000</span><span class="sxs-lookup"><span data-stu-id="30279-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-196">CA</span><span class="sxs-lookup"><span data-stu-id="30279-196">CA</span></span></p></td>
<td><p><span data-ttu-id="30279-197">San Diego</span><span class="sxs-lookup"><span data-stu-id="30279-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="30279-198">600.000</span><span class="sxs-lookup"><span data-stu-id="30279-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30279-199">**Filho2**</span><span class="sxs-lookup"><span data-stu-id="30279-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30279-200">Estado</span><span class="sxs-lookup"><span data-stu-id="30279-200">State</span></span></p></th>
<th><p><span data-ttu-id="30279-201">Cidade</span><span class="sxs-lookup"><span data-stu-id="30279-201">City</span></span></p></th>
<th><p><span data-ttu-id="30279-202">População</span><span class="sxs-lookup"><span data-stu-id="30279-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30279-203">WA</span><span class="sxs-lookup"><span data-stu-id="30279-203">WA</span></span></p></td>
<td><p><span data-ttu-id="30279-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="30279-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="30279-205">700.000</span><span class="sxs-lookup"><span data-stu-id="30279-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-206">WA</span><span class="sxs-lookup"><span data-stu-id="30279-206">WA</span></span></p></td>
<td><p><span data-ttu-id="30279-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="30279-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="30279-208">500.000</span><span class="sxs-lookup"><span data-stu-id="30279-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30279-209">**Filho3**</span><span class="sxs-lookup"><span data-stu-id="30279-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30279-210">Estado</span><span class="sxs-lookup"><span data-stu-id="30279-210">State</span></span></p></th>
<th><p><span data-ttu-id="30279-211">Cidade</span><span class="sxs-lookup"><span data-stu-id="30279-211">City</span></span></p></th>
<th><p><span data-ttu-id="30279-212">População</span><span class="sxs-lookup"><span data-stu-id="30279-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30279-213">OR</span><span class="sxs-lookup"><span data-stu-id="30279-213">OR</span></span></p></td>
<td><p><span data-ttu-id="30279-214">Medford</span><span class="sxs-lookup"><span data-stu-id="30279-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="30279-215">200.000</span><span class="sxs-lookup"><span data-stu-id="30279-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30279-216">OR</span><span class="sxs-lookup"><span data-stu-id="30279-216">OR</span></span></p></td>
<td><p><span data-ttu-id="30279-217">Portland</span><span class="sxs-lookup"><span data-stu-id="30279-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="30279-218">400.000</span><span class="sxs-lookup"><span data-stu-id="30279-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30279-219">OR</span><span class="sxs-lookup"><span data-stu-id="30279-219">OR</span></span></p></td>
<td><p><span data-ttu-id="30279-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="30279-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="30279-221">300.000</span><span class="sxs-lookup"><span data-stu-id="30279-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

