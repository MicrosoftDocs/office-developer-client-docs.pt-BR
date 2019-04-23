---
title: Operação de comandos não parametrizados
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288263"
---
# <a name="operation-of-non-parameterized-commands"></a>Operação de comandos não parametrizados


**Aplica-se ao:** Access 2013, Office 2013

Para os comandos sem parâmetros, todos os comandos do provedor são executados e os **Recordsets** são criados durante a execução do comando. Se o comando for executado de forma síncrona, todos os **Recordsets** serão totalmente preenchidos. Se o modo de preenchimento assíncrono foi selecionado, o estado de preenchimento dos **Recordsets** dependerá do modo de preenchimento e do tamanho dos **Recordsets**.

Por exemplo, o *comando pai* poderia retornar **Recordsets** dos clientes de uma empresa a partir da tabela Clientes e o *comando filho* poderia retornar **Recordsets** de pedidos de todos os clientes a partir da tabela Pedidos.

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

Para relações pai e filho sem parâmetros, cada objeto **Recordset** pai e filho deve ter uma coluna em comum para associá-los. As colunas são nomeadas na cláusula RELATE, *coluna pai* primeiro e depois *coluna filho*. As colunas podem ter nomes diferentes nos respectivos objetos **Recordset**, mas devem se referir às mesmas informações para especificar uma relação significativa. Por exemplo, os objetos **Customers** e **Orders** e **Recordset** não poderiam ter ambos um campo customerID. Como a associação do **Recordset** filho é determinada pelo comando do provedor, é possível que esse **Recordset** tenha linhas órfãs. Essas linhas são inacessíveis sem a alteração posterior da forma.

O data shaping acrescenta uma coluna de capítulo ao **Recordset** pai. Os valores na coluna de capítulo se referem às linhas do **Recordset** filho, o que está de acordo com a cláusula RELATE, ou seja, o mesmo valor está na *coluna pai* de uma determinada linha pai assim como está na *coluna filho* de todas as linhas do capítulo filho. Quando várias cláusulas TO são usadas na mesma cláusula RELATE, essas cláusulas estão implicitamente combinadas pelo uso do operador AND. Se as colunas pai na cláusula relacionada não se constituem em uma chave para o **Recordset** pai, uma única linha filha pode ter várias linhas pai.

Quando você acessa a referência na coluna de capítulo, o ADO recupera automaticamente o **Recordset** representado pela referência. Observe que em um comando sem parâmetros, ainda que o **Recordset** filho inteiro possa ser recuperado, o capítulo apresentará somente um subconjunto de linhas.

Se a coluna acrescentada não tiver um *alias de capítulo*, será gerado um nome para ela automaticamente. Um objeto [Field](field-object-ado.md) para a coluna será acrescentado à coleção [Fields](fields-collection-ado.md) do objeto **Recordset** e esse tipo de dados será **adChapter**.

Para obter informações sobre como navegar em um **Recordset** hierárquico, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).

