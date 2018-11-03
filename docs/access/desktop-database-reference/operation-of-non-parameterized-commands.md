---
title: Operação dos comandos sem parâmetros
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eac0297f2895ba78c1ff2746edcd532e79b1fa0c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944890"
---
# <a name="operation-of-non-parameterized-commands"></a>Operação dos comandos sem parâmetros


**Aplica-se a**: Access 2013, o Office 2013

Para os comandos sem parâmetros, todos os comandos do provedor são executados e os **Recordsets** são criados durante a execução do comando. Se o comando for executado de forma síncrona, todos os **Recordsets** serão totalmente preenchidos. Se o modo de preenchimento assíncrono foi selecionado, o estado de preenchimento dos **Recordsets** dependerá do modo de preenchimento e do tamanho dos **Recordsets**.

Por exemplo, o *parent-command* poderia retornar um **conjunto de registros** de clientes para uma empresa de uma tabela de clientes e o *filho-command* poderia retornar um **Recordset** de pedidos para todos os clientes de uma tabela Pedidos.

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

Para relações pai e filho sem parâmetros, cada objeto **Recordset** pai e filho deve ter uma coluna em comum para associá-los. As colunas são nomeadas na cláusula RELATE, *coluna pai* primeiro e, em seguida, a *coluna filho*. As colunas podem ter nomes diferentes nos respectivos objetos **Recordset**, mas devem se referir às mesmas informações para especificar uma relação significativa. Por exemplo, os objetos **Customers** e **Orders** e **Recordset** não poderiam ter ambos um campo customerID. Como a associação do **Recordset** filho é determinada pelo comando do provedor, é possível que esse **Recordset** tenha linhas órfãs. Essas linhas são inacessíveis sem a alteração posterior da forma.

Data shaping acrescenta uma coluna de capítulo ao **Recordset**pai. Os valores na coluna de capítulo são referências às linhas do **Recordset**, filho que satisfazem cláusula RELATE. Ou seja, o mesmo valor é na *coluna pai* de uma linha pai determinado como está na *coluna filha* de todas as linhas do filho capítulo. Quando várias cláusulas para são usadas na mesma cláusula RELATE, eles são combinados implicitamente usando um operador AND. Se as colunas pai na cláusula relate não constituem uma chave ao **Recordset**pai, uma linha única filho pode ter várias linhas pai.

Quando você acessa a referência na coluna de capítulo, o ADO recupera automaticamente o **Recordset** representado pela referência. Observe que em um comando sem parâmetros, ainda que o **Recordset** filho inteiro possa ser recuperado, o capítulo apresentará somente um subconjunto de linhas.

Se a coluna acrescentada não tiver um *alias de capítulo*, será gerado um nome para ela automaticamente. Um objeto [Field](field-object-ado.md) para a coluna será acrescentado à coleção [Fields](fields-collection-ado.md) do objeto **Recordset** e esse tipo de dados será **adChapter**.

Para obter informações sobre como navegar em um **Recordset** hierárquico, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).

