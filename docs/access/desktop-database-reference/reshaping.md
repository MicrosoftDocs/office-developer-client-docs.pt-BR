---
title: Remodelagem (referência da área de trabalho do banco de dados do Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9e0f8e017e91152ed876b933e0c0c01a7f355e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465454"
---
# <a name="reshaping"></a>Alterando a forma


**Aplica-se a**: Access 2013 | Office 2013

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

A segunda função é para permitir o acesso não dividido em objetos de **Recordset** filho existentes, usando a sintaxe `"SHAPE <recordset reshape name>"`.


> [!NOTE]
> <P>[!OBSERVAçãO] Você não pode anexar colunas a um <STRONG>Recordset</STRONG> existente, alterar a forma de um <STRONG>Recordset</STRONG> parametrizado nem os objetos <STRONG>Recordset</STRONG> em qualquer cláusula COMPUTE intermediária ou executar operações agregadas em qualquer <STRONG>Recordset</STRONG> descendente a partir do <STRONG>Recordset</STRONG> que está tendo sua forma alterada. O <STRONG>Recordset</STRONG> que está tendo sua forma alterada e o novo comando shape devem usar a mesma <A href="connection-object-ado.md">Conexão</A>.</P>


