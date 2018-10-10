---
title: Visual Basic (referência de banco de dados da área de trabalho do Access)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eeac988a85f9ef1551d740940d326b67355c478c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465214"
---
# <a name="visual-basic"></a>Visual Basic


**Aplica-se a**: Access 2013 | Office 2013

Para manipular eventos do ADO no Microsoft Visual Basic, você deve declarar uma variável no nível do módulo usando a palavra-chave **WithEvents**. É possível declarar a variável somente como parte de um módulo de classe e é necessário declará-la no nível do módulo. Contudo, isso não é tão restritivo como parece porque os objetos **Form** do Visual Basic também são classes. A maneira mais simples de tratar eventos do ADO consiste em declarar uma variável usando **WithEvents**. O exemplo a seguir trata o evento **ConnectComplete** de um objeto **Connection**:

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

O objeto **Connection** é declarado no nível de **Form** por meio da palavra-chave **WithEvents** para ativar o tratamento de eventos. O formulário\_manipulador de evento Load realmente cria o objeto, atribuindo um novo objeto de **Conexão** a *connEvent* e abre a conexão. Obviamente, um aplicativo real faria mais processamento no formato\_manipulador de eventos de carga que é mostrado aqui.
