---
title: 'Etapa 6: As alterações são enviadas ao servidor (tutorial RDS)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d26ca621ba7102dc0f9c6219ba3a16b28138770f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463441"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a>Etapa 6: As alterações são enviadas ao servidor (tutorial RDS)


**Aplica-se a**: Access 2013 | Office 2013

Se o objeto **Recordset** for editado, todas as alterações (ou seja, linhas que são incluídas, alteradas ou excluídas) poderão ser enviadas de volta ao servidor.


> [!NOTE]
> <P>O comportamento padrão do RDS pode ser chamado implicitamente com os objetos ADO e o Microsoft OLE DB Remoting Provider. As consultas podem retornar <STRONG>Recordset</STRONG>s e os <STRONG>Recordset</STRONG>s editados podem atualizar a origem de dados. Esse tutorial não chama o RDS com objetos ADO, mas veja como seria se o fizesse:</P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

**Parte A** 

Supor que, nesse caso, que você usou apenas o [RDS. DataControl](datacontrol-object-rds.md) e se um objeto **Recordset** é agora associado a **RDS. DataControl**. O método [SubmitChanges](submitchanges-method-rds.md) atualiza a origem de dados com todas as alterações ao objeto **Recordset** se as propriedades [Server](server-property-rds.md) e [Connect](connect-property-rds.md) ainda estiverem definidas.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

**Parte B** 

Como alternativa, você poderia atualizar o servidor com o objeto [rdsserver. DataFactory](datafactory-object-rdsserver.md) , especificando uma conexão e um objeto **Recordset** .

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

**Esse é o fim do tutorial.**

