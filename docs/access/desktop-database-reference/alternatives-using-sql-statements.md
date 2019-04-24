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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297148"
---
# <a name="alternatives-using-sql-statements"></a>Alternativas: Uso de instruções SQL


**Aplica-se ao:** Access 2013, Office 2013

O ADO também permite usar comandos como alternativas para as suas propriedades e métodos internos para edição de dados. Dependendo do provedor, todas as operações mencionadas neste capítulo também poderiam ser realizadas passando-se os comandos para a fonte de dados. Por exemplo, as instruções SQL UPDATE podem ser usadas para modificar os dados sem o uso da propriedade **Value** de um **Campo**. As instruções SQL INSERT podem ser usadas para adicionar novos registros a uma fonte de dados, em vez do método **AddNew** do ADO. Para obter mais informações sobre o SQL ou a linguagem de manipulação de dados do provedor, consulte a documentação da fonte de dados.

Por exemplo, é possível passar uma sequência de caracteres do SQL que contenha a instrução DELETE para um banco de dados, como mostra este código:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

