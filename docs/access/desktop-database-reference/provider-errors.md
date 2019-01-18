---
title: Erros do provedor (referência de banco de dados da área de trabalho do Access)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d175cdaa007a354d12304dceff0352a923de2291
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717640"
---
# <a name="provider-errors"></a><span data-ttu-id="7795a-102">Erros do provedor</span><span class="sxs-lookup"><span data-stu-id="7795a-102">Provider errors</span></span>


<span data-ttu-id="7795a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7795a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="7795a-p101">Quando ocorre um erro do provedor, é retornado um erro em tempo de execução de -2147467259. Quando você receber esse erro, verifique a coleção **Errors** do objeto **Connection** ativo, que conterá um ou mais erros descrevendo o que aconteceu.</span><span class="sxs-lookup"><span data-stu-id="7795a-p101">When a provider error occurs, a run-time error of -2147467259 is returned. When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="7795a-106">A coleção de erros do ADO</span><span class="sxs-lookup"><span data-stu-id="7795a-106">The ADO Errors Collection</span></span>

<span data-ttu-id="7795a-p102">Como uma determinada operação do ADO pode produzir vários erros de provedor, o ADO expõe uma coleção de objetos de erro através do objeto **Connection**. Essa coleção não conterá nenhum objeto se uma operação for concluída com êxito e conterá um ou mais objetos **Error** se algo der errado e o provedor tiver gerado um ou mais erros. Examine cada objeto de erro individual para determinar a cauxa exata do erro.</span><span class="sxs-lookup"><span data-stu-id="7795a-p102">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object. This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors. Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="7795a-p103">Quando terminar o tratamento dos erros que ocorreram, você poderá limpar a coleção chamando o método **Clear**. É especialmente importante limpar explicitamente a coleção **Errors** antes de chamar os métodos **Resync**, **UpdateBatch** ou **CancelBatch** em um objeto **Recordset**, o método **Open** em um objeto **Connection** ou definir a propriedade **Filter** em um objeto **Recordset**. Limpando a coleção explicitamente, você terá certeza de que todos os objetos **Error** na coleção não foram deixados por uma operação anterior.</span><span class="sxs-lookup"><span data-stu-id="7795a-p103">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method. It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object. By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="7795a-p104">Algumas operações podem gerar avisos e erros. Os avisos também são representados por objetos **Error** na coleção **Errors**. Quando um provedor adiciona um aviso à coleção, ele não gera um erro em tempo de execução. Verifique a propriedade **Count** da coleção **Errors** para determinar se um aviso foi produzido por uma determinada operação. Se a contagem for um ou maior, um objeto **Error** terá sido adicionado à coleção. Depois de ter determinado que a coleção **Errors** contém erros ou avisos, você poderá percorrer a coleção e recuperar informações sobre cada objeto **Error** que ela contém. O breve exemplo em Visual Basic a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="7795a-p104">Some operations can generate warnings as well as errors. Warnings are also represented by **Error** objects in the **Errors** collection. When a provider adds a warning to the collection, it does not generate a run-time error. Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation. If the count is one or greater, an **Error** object has been added to the collection. Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains. The following short Visual Basic example demonstrates this:</span></span>

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

<span data-ttu-id="7795a-p105">A rotina de tratamento de erros inclui um loop **For Each** que examina cada objeto na coleção **Errors**. Nesse exemplo, ele simplesmente acumula uma mensagem para exibição. Em um programa em funcionamento, você escreveria o código para executar uma tarefa apropriada para cada erro, como fechar todos os arquivos abertos e encerrar o programa de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="7795a-p105">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection. In this example, it simply accumulates a message for display. In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="7795a-123">O objeto Error</span><span class="sxs-lookup"><span data-stu-id="7795a-123">The Error Object</span></span>

<span data-ttu-id="7795a-p106">Examinando um objeto **Error** você pode determinar que erro ocorreu e, mais importante, qual aplicativo ou objeto causou o erro. O objeto **Error** tem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="7795a-p106">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error. The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7795a-126">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="7795a-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="7795a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="7795a-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7795a-128"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="7795a-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="7795a-129">Um texto de descrição do erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7795a-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7795a-130"><strong>HelpContext, HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="7795a-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="7795a-131">Referem-se ao tópico da Ajuda e ao arquivo da Ajuda que contêm uma descrição do erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7795a-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7795a-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="7795a-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="7795a-133">O número do erro específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="7795a-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7795a-134"><strong>Número</strong></span><span class="sxs-lookup"><span data-stu-id="7795a-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="7795a-135">Um Long Integer que representa o número (listado no <strong>ErrorValueEnum</strong>) do erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7795a-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7795a-136"><strong>Fonte</strong></span><span class="sxs-lookup"><span data-stu-id="7795a-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="7795a-137">Indica o nome do objeto ou aplicativo que gerou um erro.</span><span class="sxs-lookup"><span data-stu-id="7795a-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7795a-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="7795a-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="7795a-139">Um código de erro com cinco caracteres que o provedor retorna durante o processo de uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="7795a-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7795a-p107">O objeto **Error** do ADO é bastante semelhante ao objeto **Err** do Visual Basic padrão. Suas propriedades descrevem o erro que ocorreu. Além do número do erro, você também recebe duas informações relacionadas. A propriedade **NativeError** contém um número de erro específico do provedor que você está usando. No exemplo anterior, o provedor era o Microsoft OLE DB Provider for SQL Server, então **NativeError** conterá erros específicos do SQL Server. A propriedade **SQLState** tem um código com cinco letras que descreve um erro em uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="7795a-p107">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object. Its properties describe the error that occurred. In addition to the number of the error, you also receive two related pieces of information. The **NativeError** property contains an error number specific to the provider you are using. In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server. The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="7795a-146">Erros relacionados a eventos</span><span class="sxs-lookup"><span data-stu-id="7795a-146">Event-Related Errors</span></span>

<span data-ttu-id="7795a-p108">O objeto **Error** também é usado quando ocorrem erros relacionados a eventos. Você pode determinar se um erro ocorreu no processo que gerou um evento do ADO verificando o objeto **Error** passado como um parâmetro do evento.</span><span class="sxs-lookup"><span data-stu-id="7795a-p108">The **Error** object is also used when event-related errors occur. You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="7795a-p109">Se a operação que causa um evento é concluída com êxito, o parâmetro *adStatus* do manipulador de eventos será definido como *adStatusOK*. Por outro lado, se a operação que gerou o evento não teve êxito, o parâmetro *adStatus* é definido como *adStatusErrorsOccurred*. Nesse caso, o parâmetro *pError* conterá um objeto **Error** que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="7795a-p109">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*. On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*. In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

