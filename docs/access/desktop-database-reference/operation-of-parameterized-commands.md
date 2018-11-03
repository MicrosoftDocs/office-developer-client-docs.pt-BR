---
title: Operação dos comandos parametrizados
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd5b694906e8c0ac1f15329f4342586793e114ec
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946144"
---
# <a name="operation-of-parameterized-commands"></a>Operação dos comandos parametrizados

**Aplica-se a**: Access 2013, o Office 2013

Se você estiver trabalhando com um **Recordset** filho grande, especialmente em comparação com o tamanho do **Recordset** pai, mas precisar acessar apenas alguns capítulos do filho, poderá achar mais eficiente usar um comando com parâmetros.

Um *comando sem parâmetros* recupera o inteiro pai e filho **Recordsets**, acrescenta uma coluna de capítulo ao pai e, em seguida, atribui uma referência para o capítulo filho relacionados para cada linha pai.

Um *comando parametrizado* recupera o **Recordset**pai inteira, mas recupera apenas o capítulo **Recordset** quando a coluna de capítulo é acessada. Essa diferença na estratégia de recuperação pode produzir melhoras significativas no desempenho.

Por exemplo, você pode especificar o seguinte:

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

As tabelas pai e filho têm um nome de coluna em comum, com custo\_id *.* O *comando filho* tem um espaço reservado "?", ao qual se refere a cláusula RELATE (ou seja, "... PARÂMETRO 0").


> [!NOTE]
> <P>[!OBSERVAçãO] A cláusula PARAMETER refere-se apenas à sintaxe do comando shape. Ela não está associada ao objeto <A href="parameter-object-ado.md">Parameter</A> do ADO ou à coleção <A href="parameters-collection-ado.md">Parameters</A>.</P>



Quando o comando shape com parâmetros é executado, ocorre o seguinte:

1.  O *parent-command* é executado e retorna um **Recordset** pai da tabela Customers.

2.  Uma coluna de capítulo é acrescentada ao **Recordset** pai.

3.  Quando a coluna de capítulo de uma linha pai é acessada, o *filho-command* é executado usando o valor do customer.cust\_id como o valor do parâmetro.

4.  Todas as linhas do conjunto de linhas do provedor de dados criado na etapa 3 são usadas para preencher o **Recordset** filho. Neste exemplo, que é a todas as linhas na tabela de pedidos nos quais o com custo\_id é igual ao valor de customer.cust\_id. Por padrão, o **Recordset**s filho será armazenada na cache no cliente até que todas as referências ao **Recordset** pai sejam liberadas. Para alterar esse comportamento, defina o **Recordset** [propriedade dinâmica](ado-dynamic-property-index.md)**Linhas filho de Cache** como **False**.

5.  Uma referência às linhas filhas recuperadas (ou seja, o capítulo do **Recordset** filho) é colocada na coluna de capítulo da linha atual do **Recordset** pai.

6.  As etapas 3 a 5 serão repetidas quando for acessada a coluna de capítulo de outra linha.

A propriedade dinâmica **Cache Child Rows** é definida como **True** por padrão. O comportamento de cache varia dependendo dos valores de parâmetros da consulta. Em uma consulta com um único parâmetro, o **Recordset** filho de um dado valor de parâmetro será armazenado em cache entre as solicitações de um filho com esse valor. O código a seguir demonstra isso:

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

Em uma consulta com dois ou mais parâmetros, um filho armazenado em cache será usado apenas se todos os valores de parâmetros corresponderem aos valores armazenados em cache.

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Comandos com parâmetros e relações complexas entre pais e filhos

Além de usar comandos com parâmetros para melhorar o desempenho de uma hierarquia do tipo junção de igualdade, os comandos com parâmetros podem ser usados para oferecer suporte a relações pai-filho mais complexas. Por exemplo, considere um banco de dados de pouca liga com duas tabelas: one consistindo as equipes (equipe\_id, equipe\_nome) e o outro dos jogos (data, residencial\_equipe, visitando\_equipe).

Usando uma hierarquia sem parâmetros, não há uma maneira de relacionar as tabelas de times e de jogos de maneira que o **Recordset** filho para cada time contenha sua agenda completa. Você pode criar capítulos que contenham a agenda local ou a agenda de viagem, mas não as duas. Isso porque a cláusula RELATE o limita à relação pai-filho do formulário (pc1=cc1) AND (pc2=pc2). Isso, se o comando inclui "relacionar equipe\_inicial de para id\_equipe, a equipe\_id do visitando\_equipe", você obterá apenas jogos onde foi reproduzir uma equipe em si. O que você deseja é "(equipe\_id = home\_equipe) ou (equipe\_id = visitando\_equipe)", mas o provedor de forma não oferece suporte a cláusula OR.

Para obter o resultado desejado, você pode usar um comando com parâmetros. Por exemplo:

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Esse exemplo explora a maior flexibilidade da cláusula SQL WHERE para obter o resultado necessário.

