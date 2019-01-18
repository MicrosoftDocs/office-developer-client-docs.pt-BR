---
title: 'Alternativas: Uso de instruções SQL'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 185f5c1eb7e11a9425ff6cc4a16f1387424f3219
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711347"
---
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="d2050-102">Alternativas: Uso de instruções SQL</span><span class="sxs-lookup"><span data-stu-id="d2050-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="d2050-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2050-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2050-p101">O ADO também permite usar comandos como alternativas para as suas propriedades e métodos internos para edição de dados. Dependendo do provedor, todas as operações mencionadas neste capítulo também poderiam ser realizadas passando-se os comandos para a fonte de dados. Por exemplo, as instruções SQL UPDATE podem ser usadas para modificar os dados sem o uso da propriedade **Value** de um **Campo**. As instruções SQL INSERT podem ser usadas para adicionar novos registros a uma fonte de dados, em vez do método **AddNew** do ADO. Para obter mais informações sobre o SQL ou a linguagem de manipulação de dados do provedor, consulte a documentação da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="d2050-p101">ADO also allows using commands as alternatives to its built-in properties and methods for editing data. Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source. For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**. SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**. For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="d2050-109">Por exemplo, é possível passar uma sequência de caracteres do SQL que contenha a instrução DELETE para um banco de dados, como mostra este código:</span><span class="sxs-lookup"><span data-stu-id="d2050-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

