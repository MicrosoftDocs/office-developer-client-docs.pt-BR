---
title: 'Alternativas: Usando instruções SQL'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcda13d8b785f1048890d1ed9492f5da3e7288b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945555"
---
# <a name="alternatives-using-sql-statements"></a>Alternativas: Usando instruções SQL


**Aplica-se a**: Access 2013, o Office 2013

O ADO também permite usar comandos como alternativas para as suas propriedades e métodos internos para edição de dados. Dependendo do provedor, todas as operações mencionadas neste capítulo também poderiam ser realizadas passando-se os comandos para a fonte de dados. Por exemplo, as instruções SQL UPDATE podem ser usadas para modificar os dados sem o uso da propriedade **Value** de um **Campo**. As instruções SQL INSERT podem ser usadas para adicionar novos registros a uma fonte de dados, em vez do método **AddNew** do ADO. Para obter mais informações sobre o SQL ou a linguagem de manipulação de dados do provedor, consulte a documentação da fonte de dados.

Por exemplo, é possível passar uma sequência de caracteres do SQL que contenha a instrução DELETE para um banco de dados, como mostra este código:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

