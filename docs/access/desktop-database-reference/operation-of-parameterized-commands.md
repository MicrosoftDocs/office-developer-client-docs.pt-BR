---
title: Operação de comandos parametrizados
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288284"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="d5a53-102">Operação de comandos parametrizados</span><span class="sxs-lookup"><span data-stu-id="d5a53-102">Operation of parameterized commands</span></span>

<span data-ttu-id="d5a53-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5a53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5a53-104">Se você estiver trabalhando com um **Recordset** filho grande, especialmente em comparação com o tamanho do **Recordset** pai, mas precisar acessar apenas alguns capítulos do filho, poderá achar mais eficiente usar um comando com parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d5a53-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="d5a53-105">Um *comando sem parâmetros* recupera os **Recordsets** pai e filho completos, acrescenta uma coluna de capítulo ao pai e atribui uma referência ao capítulo filho relacionado para cada linha pai.</span><span class="sxs-lookup"><span data-stu-id="d5a53-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="d5a53-p101">Um *comando com parâmetros* recupera todo o **Recordset** pai, mas recupera apenas o **Recordset** do capítulo quando a coluna do capítulo é acessada. Essa diferença na estratégia de recuperação pode produzir melhoras significativas no desempenho.</span><span class="sxs-lookup"><span data-stu-id="d5a53-p101">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed. This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="d5a53-108">Por exemplo, você pode especificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5a53-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="d5a53-109">As tabelas pai e filho têm um nome de coluna em comum ID\_de cust *.*</span><span class="sxs-lookup"><span data-stu-id="d5a53-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="d5a53-110">O *filho-Command* tem um marcador de "?", ao qual a cláusula relate se refere (ou seja, "... PARÂMETRO 0 ").</span><span class="sxs-lookup"><span data-stu-id="d5a53-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="d5a53-p103">[!OBSERVAçãO] A cláusula PARAMETER refere-se apenas à sintaxe do comando shape. Ela não está associada ao objeto [Parameter](parameter-object-ado.md) do ADO ou à coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d5a53-p103">The PARAMETER clause pertains solely to the shape command syntax. It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="d5a53-113">Quando o comando shape com parâmetros é executado, ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5a53-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="d5a53-114">O *parent-command* é executado e retorna um **Recordset** pai da tabela Clientes.</span><span class="sxs-lookup"><span data-stu-id="d5a53-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="d5a53-115">Uma coluna de capítulo é acrescentada ao **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="d5a53-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="d5a53-116">Quando a coluna de capítulo de uma linha pai é acessada, o *comando Child-Command* é executado usando o valor da\_ID Customer. cust como o valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5a53-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="d5a53-117">Todas as linhas do conjunto de linhas do provedor de dados criado na etapa 3 são usadas para preencher o **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="d5a53-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="d5a53-118">Neste exemplo, todas as linhas da tabela Orders em que a ID de cust\_é igual ao valor de Customer. cust\_ID.</span><span class="sxs-lookup"><span data-stu-id="d5a53-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="d5a53-119">Por padrão, o **Recordset** filho será armazenado em cache no cliente até que todas as referências ao **Recordset** pai sejam liberadas.</span><span class="sxs-lookup"><span data-stu-id="d5a53-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="d5a53-120">Para alterar esse comportamento, defina as**linhas filhas do cache** de [propriedades dinâmicas](ado-dynamic-property-index.md)do **Recordset** como **false**.</span><span class="sxs-lookup"><span data-stu-id="d5a53-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="d5a53-121">Uma referência às linhas filhas recuperadas (ou seja, o capítulo do **Recordset** filho) é colocada na coluna de capítulo da linha atual do **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="d5a53-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="d5a53-122">As etapas 3 a 5 serão repetidas quando for acessada a coluna de capítulo de outra linha.</span><span class="sxs-lookup"><span data-stu-id="d5a53-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="d5a53-p105">A propriedade dinâmica **Cache Child Rows** é definida como **True** por padrão. O comportamento de cache varia dependendo dos valores de parâmetros da consulta. Em uma consulta com um único parâmetro, o **Recordset** filho de um dado valor de parâmetro será armazenado em cache entre as solicitações de um filho com esse valor. O código a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="d5a53-p105">The **Cache Child Rows** dynamic property is set to **True** by default. The caching behavior varies depending upon the parameter values of the query. In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value. The following code demonstrates this:</span></span>

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

<span data-ttu-id="d5a53-127">Em uma consulta com dois ou mais parâmetros, um filho armazenado em cache será usado apenas se todos os valores de parâmetros corresponderem aos valores armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="d5a53-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="d5a53-128">Comandos com parâmetros e relações filho complexas pai</span><span class="sxs-lookup"><span data-stu-id="d5a53-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="d5a53-129">Além de usar comandos com parâmetros para melhorar o desempenho de uma hierarquia do tipo junção de igualdade, os comandos com parâmetros podem ser usados para oferecer suporte a relações pai-filho mais complexas.</span><span class="sxs-lookup"><span data-stu-id="d5a53-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="d5a53-130">Por exemplo, considere um pequeno banco de dados de League com duas tabelas: uma que consiste em equipes\_(ID da\_equipe, nome da equipe) e a outra de jogos\_(data,\_equipe inicial, equipe de visita).</span><span class="sxs-lookup"><span data-stu-id="d5a53-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="d5a53-131">Usando uma hierarquia sem parâmetros, não há uma maneira de relacionar as tabelas de times e de jogos de maneira que o **Recordset** filho para cada time contenha sua agenda completa.</span><span class="sxs-lookup"><span data-stu-id="d5a53-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="d5a53-132">Você pode criar capítulos que contenham a agenda local ou a agenda de viagem, mas não as duas.</span><span class="sxs-lookup"><span data-stu-id="d5a53-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="d5a53-133">Isso porque a cláusula RELATE o limita à relação pai-filho do formulário (pc1=cc1) AND (pc2=pc2).</span><span class="sxs-lookup"><span data-stu-id="d5a53-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="d5a53-134">Portanto, se o seu comando incluiu "\_relacionar ID\_de equipe para\_equipe inicial,\_ID de equipe para a equipe de visita", você receberia apenas jogos em que a equipe estava jogando.</span><span class="sxs-lookup"><span data-stu-id="d5a53-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="d5a53-135">O que você deseja é "(\_ID de equipe\_= equipe inicial) ou\_(ID de\_equipe = equipe de visita)", mas o provedor de forma não tem suporte para a cláusula or.</span><span class="sxs-lookup"><span data-stu-id="d5a53-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="d5a53-p108">Para obter o resultado desejado, você pode usar um comando com parâmetros. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d5a53-p108">To obtain the desired result, you can use a parameterized command. For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="d5a53-138">Esse exemplo explora a maior flexibilidade da cláusula SQL WHERE para obter o resultado necessário.</span><span class="sxs-lookup"><span data-stu-id="d5a53-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

