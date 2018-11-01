---
title: Erros do ActiveX Data Objects (ADO)
TOCTitle: ADO Errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66b0d7ca54723755bcdb6e24726f75836cd9716f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885637"
---
# <a name="ado-errors"></a><span data-ttu-id="bb09f-102">Erros do ADO</span><span class="sxs-lookup"><span data-stu-id="bb09f-102">ADO Errors</span></span>


<span data-ttu-id="bb09f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb09f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb09f-104">Os erros do ADO são relatados para o seu programa como erros em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bb09f-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="bb09f-105">Você pode usar o mecanismo de interceptação de erro da sua linguagem de programação para interceptá-los e tratá-los.</span><span class="sxs-lookup"><span data-stu-id="bb09f-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="bb09f-106">Por exemplo, no Visual Basic, use a instrução **On Error**.</span><span class="sxs-lookup"><span data-stu-id="bb09f-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="bb09f-107">No Visual J++, use um bloco **try-catch**.</span><span class="sxs-lookup"><span data-stu-id="bb09f-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="bb09f-108">No Visual C++, depende do método que estiver sendo usado para acessar as bibliotecas do ADO.</span><span class="sxs-lookup"><span data-stu-id="bb09f-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="bb09f-109">Com \#importar, use um bloco **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="bb09f-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="bb09f-110">Caso contrário, os programadores do C++ precisarão recuperar de maneira explícita o objeto de erro chamando **GetErrorInfo**.</span><span class="sxs-lookup"><span data-stu-id="bb09f-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="bb09f-111">O seguinte subprocedimento do Visual Basic demonstra a interceptação de um erro do ADO:</span><span class="sxs-lookup"><span data-stu-id="bb09f-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="bb09f-112">Isso **formulário\_carga** procedimento de evento intencionalmente cria um erro ao tentar abrir o mesmo objeto de **Conexão** duas vezes.</span><span class="sxs-lookup"><span data-stu-id="bb09f-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="bb09f-113">Na segunda vez que o método **Open** é chamado, o identificador de erro é ativado.</span><span class="sxs-lookup"><span data-stu-id="bb09f-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="bb09f-114">Nesse caso, o erro é do tipo **adErrObjectOpen**, portanto, o identificador de erro exibe a seguinte mensagem antes de continuar a execução do programa:</span><span class="sxs-lookup"><span data-stu-id="bb09f-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="bb09f-p103">A mensagem de erro inclui cada informação fornecida pelo objeto **Err** do Visual Basic, exceto o valor **LastDLLError**, que não se aplica neste caso. O número informa qual erro ocorreu. A descrição é útil nos casos em você não deseja tratar o erro por conta própria. Basta passá-lo para o usuário. Embora você geralmente use mensagens personalizadas para o seu aplicativo, não poderá prever todos os erros; a descrição fornece alguma dica sobre o que aconteceu de errado. No código de exemplo, o erro foi relatado pelo objeto **Connection**. Aqui você verá o tipo do objeto ou a identificação programática  não um nome de variável.</span><span class="sxs-lookup"><span data-stu-id="bb09f-p103">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here. The error number tells you which error has occurred. The description is useful in cases in which you do not want to handle the error yourself. You can simply pass it along to the user. Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong. In the sample code, the error was reported by the **Connection** object. You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="bb09f-p104">[!OBSERVAçãO] O objeto **Err** do Visual Basic contém apenas informações sobre o erro mais recente. A coleção **Errors** do objeto **Connection** do ADO contém um objeto **Error** para cada erro provocado pela operação mais recente do ADO. Use a coleção **Errors** em vez do objeto **Err** para identificar vários erros. Para obter mais informações sobre a coleção **Errors**, consulte <A href="provider-errors.md">Erros do provedor</A>. No entanto, se não houver nenhum objeto **Connection** válido, o objeto **Err** será a única fonte de informações sobre os erros do ADO.</span><span class="sxs-lookup"><span data-stu-id="bb09f-p104">The Visual Basic **Err** object only contains information about the most recent error. The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation. Use the **Errors** collection rather than the **Err** object to handle multiple errors. For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>. However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="bb09f-p105">Que tipos de operações provavelmente causam erros do ADO? Os erros comuns do ADO podem envolver a abertura de um objeto como **Connection** ou **Recordset**, a tentativa de atualizar dados, ou a chamada de um método ou propriedade para o qual o provedor não ofereça suporte.</span><span class="sxs-lookup"><span data-stu-id="bb09f-p105">What kinds of operations are likely to cause ADO errors? Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="bb09f-p106">Os erros do OLE DB também podem ser passados para o aplicativo como erros em tempo de execução na coleção **Errors**. Para obter mais informações sobre números de erros do OLE DB, consulte o Capítulo 16 da Referência do programador do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="bb09f-p106">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection. For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

