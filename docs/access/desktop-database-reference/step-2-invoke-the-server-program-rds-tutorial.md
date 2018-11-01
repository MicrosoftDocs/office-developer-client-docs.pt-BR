---
title: 'Etapa 2: Chamar o programa do servidor (tutorial RDS)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53ad3306bf9e175566f0a3d02b1454872264d4b6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885476"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a>Etapa 2: Chamar um programa do servidor (Tutorial do RDS)


**Aplica-se a**: Access 2013, o Office 2013

Ao chamar um método no *proxy* do cliente, o programa real no servidor executa o método. Nessa etapa, você executará uma consulta no servidor.

**Parte A** Se você não estava usando [Rdsserver](datafactory-object-rdsserver.md) neste tutorial, a maneira mais conveniente executar esta etapa seria usar o [RDS. DataControl](datacontrol-object-rds.md) objeto. O **RDS.DataControl** combina a etapa anterior da criação de um proxy, com essa etapa, emitindo a consulta.

Defina a propriedade **Server** do objeto [RDS.DataControl](server-property-rds.md) para identificar onde o programa do servidor deve ser instanciado; a propriedade [Connect](connect-property-rds.md) para especificar a cadeia de conexão para acessar a origem de dados; e a propriedade [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) para especificar o texto do comando de consulta. Em seguida emita o método [Refresh](refresh-method-rds.md) para fazer com que o programa do servidor se conecte à origem de dados, recuperar as linhas especificadas pela consulta e retornar um objeto **Recordset** ao cliente.

Este tutorial não usa o **RDS.DataControl**, mas veja como seria se o fizesse:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

Ele também não invoca RDS com objetos ADO, mas veja como seria se o fizesse:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

**Parte B** O método geral para realizar esta etapa é invocar o método [Query](query-method-rds.md) do objeto **Rdsserver** . Esse método assume uma cadeia de conexão, que é usada para se conectar a uma origem de dados e um texto de comando, que é usada para especificar as linhas a serem retornadas a partir da origem de dados.

Este tutorial usa o método **Query** do objeto **DataFactory**:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

