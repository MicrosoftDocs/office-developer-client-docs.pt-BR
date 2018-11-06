---
title: Operação dos comandos parametrizados
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1623b32a5ec52acd086bf028a5c1775daae989e8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997046"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="ab5cb-102">Operação dos comandos parametrizados</span><span class="sxs-lookup"><span data-stu-id="ab5cb-102">Operation of parameterized commands</span></span>

<span data-ttu-id="ab5cb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab5cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab5cb-104">Se você estiver trabalhando com um **Recordset** filho grande, especialmente em comparação com o tamanho do **Recordset** pai, mas precisar acessar apenas alguns capítulos do filho, poderá achar mais eficiente usar um comando com parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="ab5cb-105">Um *comando sem parâmetros* recupera o inteiro pai e filho **Recordsets**, acrescenta uma coluna de capítulo ao pai e, em seguida, atribui uma referência para o capítulo filho relacionados para cada linha pai.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="ab5cb-106">Um *comando parametrizado* recupera o **Recordset**pai inteira, mas recupera apenas o capítulo **Recordset** quando a coluna de capítulo é acessada.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="ab5cb-107">Essa diferença na estratégia de recuperação pode produzir melhoras significativas no desempenho.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="ab5cb-108">Por exemplo, você pode especificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ab5cb-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="ab5cb-109">As tabelas pai e filho têm um nome de coluna em comum, com custo\_id *.*</span><span class="sxs-lookup"><span data-stu-id="ab5cb-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="ab5cb-110">O *comando filho* tem um espaço reservado "?", ao qual se refere a cláusula RELATE (ou seja, "... PARÂMETRO 0").</span><span class="sxs-lookup"><span data-stu-id="ab5cb-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="ab5cb-p103">[!OBSERVAçãO] A cláusula PARAMETER refere-se apenas à sintaxe do comando shape. Ela não está associada ao objeto [Parameter](parameter-object-ado.md) do ADO ou à coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ab5cb-p103">The PARAMETER clause pertains solely to the shape command syntax. It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="ab5cb-113">Quando o comando shape com parâmetros é executado, ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ab5cb-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="ab5cb-114">O *parent-command* é executado e retorna um **Recordset** pai da tabela Customers.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="ab5cb-115">Uma coluna de capítulo é acrescentada ao **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="ab5cb-116">Quando a coluna de capítulo de uma linha pai é acessada, o *filho-command* é executado usando o valor do customer.cust\_id como o valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="ab5cb-117">Todas as linhas do conjunto de linhas do provedor de dados criado na etapa 3 são usadas para preencher o **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="ab5cb-118">Neste exemplo, que é a todas as linhas na tabela de pedidos nos quais o com custo\_id é igual ao valor de customer.cust\_id.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="ab5cb-119">Por padrão, o **Recordset**s filho será armazenada na cache no cliente até que todas as referências ao **Recordset** pai sejam liberadas.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="ab5cb-120">Para alterar esse comportamento, defina o **Recordset** [propriedade dinâmica](ado-dynamic-property-index.md)**Linhas filho de Cache** como **False**.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="ab5cb-121">Uma referência às linhas filhas recuperadas (ou seja, o capítulo do **Recordset** filho) é colocada na coluna de capítulo da linha atual do **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="ab5cb-122">As etapas 3 a 5 serão repetidas quando for acessada a coluna de capítulo de outra linha.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="ab5cb-p105">A propriedade dinâmica **Cache Child Rows** é definida como **True** por padrão. O comportamento de cache varia dependendo dos valores de parâmetros da consulta. Em uma consulta com um único parâmetro, o **Recordset** filho de um dado valor de parâmetro será armazenado em cache entre as solicitações de um filho com esse valor. O código a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="ab5cb-p105">The **Cache Child Rows** dynamic property is set to **True** by default. The caching behavior varies depending upon the parameter values of the query. In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value. The following code demonstrates this:</span></span>

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

<span data-ttu-id="ab5cb-127">Em uma consulta com dois ou mais parâmetros, um filho armazenado em cache será usado apenas se todos os valores de parâmetros corresponderem aos valores armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="ab5cb-128">Comandos parametrizados e relações de filho pai complexa</span><span class="sxs-lookup"><span data-stu-id="ab5cb-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="ab5cb-129">Além de usar comandos com parâmetros para melhorar o desempenho de uma hierarquia do tipo junção de igualdade, os comandos com parâmetros podem ser usados para oferecer suporte a relações pai-filho mais complexas.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="ab5cb-130">Por exemplo, considere um banco de dados de pouca liga com duas tabelas: one consistindo as equipes (equipe\_id, equipe\_nome) e o outro dos jogos (data, residencial\_equipe, visitando\_equipe).</span><span class="sxs-lookup"><span data-stu-id="ab5cb-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="ab5cb-131">Usando uma hierarquia sem parâmetros, não há uma maneira de relacionar as tabelas de times e de jogos de maneira que o **Recordset** filho para cada time contenha sua agenda completa.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="ab5cb-132">Você pode criar capítulos que contenham a agenda local ou a agenda de viagem, mas não as duas.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="ab5cb-133">Isso porque a cláusula RELATE o limita à relação pai-filho do formulário (pc1=cc1) AND (pc2=pc2).</span><span class="sxs-lookup"><span data-stu-id="ab5cb-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="ab5cb-134">Isso, se o comando inclui "relacionar equipe\_inicial de para id\_equipe, a equipe\_id do visitando\_equipe", você obterá apenas jogos onde foi reproduzir uma equipe em si.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="ab5cb-135">O que você deseja é "(equipe\_id = home\_equipe) ou (equipe\_id = visitando\_equipe)", mas o provedor de forma não oferece suporte a cláusula OR.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="ab5cb-p108">Para obter o resultado desejado, você pode usar um comando com parâmetros. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ab5cb-p108">To obtain the desired result, you can use a parameterized command. For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="ab5cb-138">Esse exemplo explora a maior flexibilidade da cláusula SQL WHERE para obter o resultado necessário.</span><span class="sxs-lookup"><span data-stu-id="ab5cb-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

