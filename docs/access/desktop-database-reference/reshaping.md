---
title: Remodelagem (referência do banco de dados da área de trabalho do Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314774"
---
# <a name="reshaping"></a>Remodelagem

**Aplica-se ao:** Access 2013, Office 2013

A um **Recordset** criado por uma cláusula de um comando shape pode ser atribuído um nome de *alias* (geralmente com a palavra-chave AS). O alias de um **Recordset** com forma pode ser mencionado em um comando totalmente diferente. Ou seja, você pode usar novamente ou *alterar a forma* de um **Recordset** com formato anterior em um novo comando shape. Para oferecer suporte a este recurso, o ADO fornece uma propriedade, [Reshape Name](reshape-name-property-dynamic-ado.md).

A alteração da forma tem duas funções principais. A primeira é associar um **Recordset** existente a um novo **Recordset** pai.

## <a name="example"></a>Exemplo

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

A segunda função é habilitar o acesso não capítulo a objetos **Recordset** filho existentes, usando a sintaxe `"SHAPE <recordset reshape name>"` .

> [!NOTE]
> [!OBSERVAçãO] Você não pode anexar colunas a um **Recordset** existente, alterar a forma de um **Recordset** parametrizado nem os objetos **Recordset** em qualquer cláusula COMPUTE intermediária ou executar operações agregadas em qualquer **Recordset** descendente a partir do **Recordset** que está tendo sua forma alterada. O **Recordset que** está sendo reshapedado e o novo comando shape devem usar o mesmo objeto **[Connection.](connection-object-ado.md)


