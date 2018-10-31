---
title: 'Capítulo 4: Edição de dados'
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d859f7bc3a74dfde1841be87f4a8237af9b7c48a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862251"
---
# <a name="chapter-4-editing-data"></a>Capítulo 4: Edição de dados


**Aplica-se a**: Access 2013 | Office 2013

Os dois capítulos anteriores explicaram como usar o ADO para estabelecer conexão com uma fonte de dados, executar um comando, obter os resultados em um objeto **Recordset** e navegar no **Recordset**. Este capítulo concentra-se na próxima operação fundamental do ADO: edição de dados.

Ele continua a usar o **Recordset** de exemplo apresentado no Capítulo 3 , com uma alteração importante. O código a seguir é usado para abrir o **Recordset**:

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

A alteração importante no código envolve a definição da propriedade **CursorLocation** do objeto **Connection** como **adUseClient** na função GetNewConnection (mostrada abaixo), que indica o uso de um cursor de cliente. Para obter mais informações sobre as diferenças entre cursores de cliente e de servidor, consulte o [Capítulo 8: Noções básicas sobre cursores e proteções](chapter-8-understanding-cursors-and-locks.md).

A definição **adUseClient** da propriedade **CursorLocation** move o local do cursor da fonte de dados (neste caso, o SQL Server) para o local do código do cliente (a estação de trabalho desktop). Essa definição força o ADO a chamar o Client Cursor Engine para OLE DB no cliente para criar e gerenciar o cursor.

Você também pode ter notado que o parâmetro **LockType** do método **Open** foi alterado para **adLockBatchOptimistic**. Essa ação abre o cursor no modo em lotes. (O provedor armazena em cache várias alterações e as grava na fonte de dados subjacente somente quando o método **UpdateBatch** é chamado.) As alterações feitas no **Recordset** só serão atualizadas no banco de dados quando o método **UpdateBatch** for chamado.

Por fim, o código neste capítulo usa uma versão modificada da função GetNewConnection, apresentada no Capítulo 2. Agora, essa versão da função retorna um cursor do cliente. A função tem esta aparência:

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

Este capítulo aborda os seguintes tópicos:

- [Edição de registros existentes](editing-existing-records.md)

- [Determinação do que é compatível](determining-what-is-supported.md)

- [Excluindo registros com o método Delete](deleting-records-using-the-delete-method.md)

- [Alternativas: Uso de instruções SQL](alternatives-using-sql-statements.md)

- [Adicionando registros (ADO)](adding-records.md)