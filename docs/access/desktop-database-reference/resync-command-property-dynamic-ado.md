---
title: Propriedade dinâmica de comando Resync (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa1fe05e6aa7edf04ad74864eb30a03403323c8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306577"
---
# <a name="resync-command-dynamic-property-ado"></a>Propriedade dinâmica de comando Resync (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Especifica uma cadeia de caracteres de comando, fornecida pelo usuário, que o método [Resync](resync-method-ado.md) emite para atualizar os dados na tabela chamada na propriedade dinâmica [Tabela exclusiva](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que é uma sequência de comandos.

## <a name="remarks"></a>Comentários

O objeto [Recordset](recordset-object-ado.md) é o resultado de um operação JOIN executada em diversas tabelas base. As linhas afetadas dependem do parâmetro *AffectRecords* do método [Resync](resync-method-ado.md). O método **Resync** padrão é executado se as propriedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e **Resync Command** não estiverem definidas.

A sequência de comandos da propriedade **Resync Command** é um comando com parâmetros ou um procedimento armazenado que identifica com exclusividade a linha que está sendo atualizada e retorna uma única linha contendo o mesmo número e ordem de colunas da linha a ser atualizada. A sequência de comandos contém um parâmetro para cada coluna de chave primária na **Unique Table**; caso contrário, um erro em tempo de execução será retornado. Os parâmetros são preenchidos automaticamente com os valores da chave primária da linha a ser atualizada.

Aqui estão dois exemplos baseados no SQL:

1.  O **Recordset** é definido por um comando:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    A propriedade **Resync Command** é definida como:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    A **Unique Table** é *Orders* e sua chave primária, *OrderID*, está parametrizada. A subseleção fornece um modo simples de garantir de maneira programática que o mesmo número e a mesma ordem de colunas serão retornados da mesma forma que pelo comando original.

2. O **Recordset** é definido por um procedimento armazenado:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    O método **Resync** deve executar o seguinte procedimento armazenado:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    A propriedade **Resync Command** é definida como:

    `"{call CustordersResync (?)}"`

Mais uma vez, a **Unique Table** é *Orders* e sua chave-primária, *OrderID*, está parametrizada.

**Resync Command** é uma propriedade dinâmica acrescentada à coleção [Properties](properties-collection-ado.md) do objeto **Recordset** quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver configurada como **adUseClient**.

