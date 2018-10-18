---
title: Propriedade Resync Command -- Dinâmica (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d9133f37b236cfa876a5d6ae8642f25f919f2cb
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602801"
---
# <a name="resync-command-property--dynamic-ado"></a>Propriedade Resync Command -- Dinâmica (ADO)

**Aplica-se a**: Access 2013 | Office 2013

Especifica uma cadeia de caracteres de comando, fornecida pelo usuário, que o método [Resync](resync-method-ado.md) emite para atualizar os dados na tabela chamada na propriedade dinâmica [Tabela exclusiva](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **String** que é uma sequência de comandos.

## <a name="remarks"></a>Comentários

O objeto [Recordset](recordset-object-ado.md) é o resultado de um operação JOIN executada em diversas tabelas base. As linhas afetadas dependem do parâmetro *AffectRecords* do método [Resync](resync-method-ado.md) . O método **Resync** padrão é executado se as propriedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e **Resync Command** não estiverem definidas.

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

**Resync Command** é uma propriedade dinâmica acrescentada à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver configurada como **adUseClient**.

