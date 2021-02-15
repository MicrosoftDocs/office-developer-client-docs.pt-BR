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
# <a name="operation-of-parameterized-commands"></a>Operação de comandos parametrizados

**Aplica-se ao:** Access 2013, Office 2013

Se você estiver trabalhando com um **Recordset** filho grande, especialmente em comparação com o tamanho do **Recordset** pai, mas precisar acessar apenas alguns capítulos do filho, poderá achar mais eficiente usar um comando com parâmetros.

Um *comando sem parâmetros* recupera os **Recordsets** pai e filho completos, acrescenta uma coluna de capítulo ao pai e atribui uma referência ao capítulo filho relacionado para cada linha pai.

Um *comando com parâmetros* recupera todo o **Recordset** pai, mas recupera apenas o **Recordset** do capítulo quando a coluna do capítulo é acessada. Essa diferença na estratégia de recuperação pode produzir melhoras significativas no desempenho.

Por exemplo, você pode especificar o seguinte:

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

As tabelas pai e filho têm um nome de coluna em comum, \_ cust id *.* O *comando filho tem* um espaço reservado "?" ao qual a cláusula RELATE se refere (ou seja, "... PARÂMETRO 0").

> [!NOTE]
> [!OBSERVAçãO] A cláusula PARAMETER refere-se apenas à sintaxe do comando shape. Ela não está associada ao objeto [Parameter](parameter-object-ado.md) do ADO ou à coleção [Parameters](parameters-collection-ado.md).

Quando o comando shape com parâmetros é executado, ocorre o seguinte:

1.  O *parent-command* é executado e retorna um **Recordset** pai da tabela Clientes.

2.  Uma coluna de capítulo é acrescentada ao **Recordset** pai.

3.  Quando a coluna de capítulo de  uma linha pai é acessada, o comando filho é executado usando o valor da ID customer.cust como o \_ valor do parâmetro.

4.  Todas as linhas do conjunto de linhas do provedor de dados criado na etapa 3 são usadas para preencher o **Recordset** filho. Neste exemplo, são todas as linhas da tabela Pedidos nas quais a ID de cust é igual ao valor da \_ \_ ID customer.cust. Por padrão, o **Recordset** filho será armazenado em cache no cliente até que todas as referências ao **Recordset** pai sejam liberadas. Para alterar esse comportamento, de definida a propriedade [dinâmica](ado-dynamic-property-index.md)**Cache Child Rows** do **Recordset** como **False**.

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

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Comandos parametrizados e relações complexas entre pais e filhos

Além de usar comandos com parâmetros para melhorar o desempenho de uma hierarquia do tipo junção de igualdade, os comandos com parâmetros podem ser usados para oferecer suporte a relações pai-filho mais complexas. Por exemplo, considere um banco de dados do Little League com duas tabelas: uma consistindo das equipes (id da equipe, nome da equipe) e a outra de jogos (data, time da casa, equipe \_ \_ \_ \_ visitante).

Usando uma hierarquia sem parâmetros, não há uma maneira de relacionar as tabelas de times e de jogos de maneira que o **Recordset** filho para cada time contenha sua agenda completa. Você pode criar capítulos que contenham a agenda local ou a agenda de viagem, mas não as duas. Isso porque a cláusula RELATE o limita à relação pai-filho do formulário (pc1=cc1) AND (pc2=pc2). Portanto, se seu comando incluísse "RELATE a ID da equipe ao time da casa, id da equipe PARA time visitante", você obteria apenas os jogos em que um time \_ \_ estivesse jogando \_ \_ sozinho. O que você deseja é "(team \_ id=home \_ team) OR (team \_ id=visiting team)", mas o provedor Shape não dá suporte à \_ cláusula OR.

Para obter o resultado desejado, você pode usar um comando com parâmetros. Por exemplo:

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Esse exemplo explora a maior flexibilidade da cláusula SQL WHERE para obter o resultado necessário.

