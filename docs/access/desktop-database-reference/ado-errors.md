---
title: Erros do ActiveX Data Objects (ADO)
TOCTitle: ADO errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a25dc0d1d5e621a610b34ca1875c3fd76ba56eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283377"
---
# <a name="ado-errors"></a>Erros do ADO

**Aplica-se ao:** Access 2013, Office 2013

Os erros do ADO são relatados para o seu programa como erros em tempo de execução. Você pode usar o mecanismo de interceptação de erro da sua linguagem de programação para interceptá-los e tratá-los. Por exemplo, no Visual Basic, use a instrução **On Error**. No Visual J++, use um bloco **try-catch**. No Visual C++, depende do método que estiver sendo usado para acessar as bibliotecas do ADO. Com \#a importação, use um bloco **try-catch** . Caso contrário, os programadores do C++ precisarão recuperar de maneira explícita o objeto de erro chamando **GetErrorInfo**. O seguinte subprocedimento do Visual Basic demonstra a interceptação de um erro do ADO:

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

Este procedimento de evento **\_Form Load** cria intencionalmente um erro tentando abrir o mesmo objeto **Connection** duas vezes. Na segunda vez que o método **Open** é chamado, o identificador de erro é ativado. Nesse caso, o erro é do tipo **adErrObjectOpen**, portanto, o identificador de erro exibe a seguinte mensagem antes de continuar a execução do programa:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

A mensagem de erro inclui cada informação fornecida pelo objeto **Err** do Visual Basic, exceto o valor **LastDLLError**, que não se aplica neste caso. O número informa qual erro ocorreu. A descrição é útil nos casos em você não deseja tratar o erro por conta própria. Basta passá-lo para o usuário. Embora você geralmente use mensagens personalizadas para o seu aplicativo, não poderá prever todos os erros; a descrição fornece alguma dica sobre o que aconteceu de errado. No código de exemplo, o erro foi relatado pelo objeto **Connection**. Aqui você verá o tipo do objeto ou a identificação programática  não um nome de variável.


> [!NOTE]
> [!OBSERVAçãO] O objeto **Err** do Visual Basic contém apenas informações sobre o erro mais recente. A coleção **Errors** do objeto **Connection** do ADO contém um objeto **Error** para cada erro provocado pela operação mais recente do ADO. Use a coleção **Errors** em vez do objeto **Err** para identificar vários erros. Para obter mais informações sobre a coleção **Errors**, consulte <A href="provider-errors.md">Erros do provedor</A>. No entanto, se não houver nenhum objeto **Connection** válido, o objeto **Err** será a única fonte de informações sobre os erros do ADO.

Que tipos de operações provavelmente causam erros do ADO? Os erros comuns do ADO podem envolver a abertura de um objeto como **Connection** ou **Recordset**, a tentativa de atualizar dados, ou a chamada de um método ou propriedade para o qual o provedor não ofereça suporte.

Os erros do OLE DB também podem ser passados para o aplicativo como erros em tempo de execução na coleção **Errors**. Para obter mais informações sobre números de erros do OLE DB, consulte o Capítulo 16 da Referência do programador do OLE DB.

