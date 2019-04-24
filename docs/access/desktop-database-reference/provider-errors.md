---
title: Erros do provedor (referência do banco de dados do Access Desktop)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d175cdaa007a354d12304dceff0352a923de2291
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301124"
---
# <a name="provider-errors"></a>Erros do provedor


**Aplica-se ao:** Access 2013, Office 2013 

Quando ocorre um erro do provedor, é retornado um erro em tempo de execução de -2147467259. Quando você receber esse erro, verifique a coleção **Errors** do objeto **Connection** ativo, que conterá um ou mais erros descrevendo o que aconteceu.

## <a name="the-ado-errors-collection"></a>A coleção de erros do ADO

Como uma determinada operação do ADO pode produzir vários erros de provedor, o ADO expõe uma coleção de objetos de erro através do objeto **Connection**. Essa coleção não conterá nenhum objeto se uma operação for concluída com êxito e conterá um ou mais objetos **Error** se algo der errado e o provedor tiver gerado um ou mais erros. Examine cada objeto de erro individual para determinar a cauxa exata do erro.

Quando terminar o tratamento dos erros que ocorreram, você poderá limpar a coleção chamando o método **Clear**. É especialmente importante limpar explicitamente a coleção **Errors** antes de chamar os métodos **Resync**, **UpdateBatch** ou **CancelBatch** em um objeto **Recordset**, o método **Open** em um objeto **Connection** ou definir a propriedade **Filter** em um objeto **Recordset**. Limpando a coleção explicitamente, você terá certeza de que todos os objetos **Error** na coleção não foram deixados por uma operação anterior.

Algumas operações podem gerar avisos e erros. Os avisos também são representados por objetos **Error** na coleção **Errors**. Quando um provedor adiciona um aviso à coleção, ele não gera um erro em tempo de execução. Verifique a propriedade **Count** da coleção **Errors** para determinar se um aviso foi produzido por uma determinada operação. Se a contagem for um ou maior, um objeto **Error** terá sido adicionado à coleção. Depois de ter determinado que a coleção **Errors** contém erros ou avisos, você poderá percorrer a coleção e recuperar informações sobre cada objeto **Error** que ela contém. O breve exemplo em Visual Basic a seguir demonstra isso:

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

A rotina de tratamento de erros inclui um loop **For Each** que examina cada objeto na coleção **Errors**. Nesse exemplo, ele simplesmente acumula uma mensagem para exibição. Em um programa em funcionamento, você escreveria o código para executar uma tarefa apropriada para cada erro, como fechar todos os arquivos abertos e encerrar o programa de maneira ordenada.

## <a name="the-error-object"></a>O objeto Error

Examinando um objeto **Error** você pode determinar que erro ocorreu e, mais importante, qual aplicativo ou objeto causou o erro. O objeto **Error** tem as seguintes propriedades:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Descrição</strong></p></td>
<td><p>Um texto de descrição do erro que ocorreu.</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext, HelpFile</strong></p></td>
<td><p>Referem-se ao tópico da Ajuda e ao arquivo da Ajuda que contêm uma descrição do erro que ocorreu.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>O número do erro específico do provedor.</p></td>
</tr>
<tr class="even">
<td><p><strong>Número</strong></p></td>
<td><p>Um Long Integer que representa o número (listado no <strong>ErrorValueEnum</strong>) do erro que ocorreu.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Fonte</strong></p></td>
<td><p>Indica o nome do objeto ou aplicativo que gerou um erro.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Um código de erro com cinco caracteres que o provedor retorna durante o processo de uma instrução SQL.</p></td>
</tr>
</tbody>
</table>


O objeto **Error** do ADO é bastante semelhante ao objeto **Err** do Visual Basic padrão. Suas propriedades descrevem o erro que ocorreu. Além do número do erro, você também recebe duas informações relacionadas. A propriedade **NativeError** contém um número de erro específico do provedor que você está usando. No exemplo anterior, o provedor era o Microsoft OLE DB Provider for SQL Server, então **NativeError** conterá erros específicos do SQL Server. A propriedade **SQLState** tem um código com cinco letras que descreve um erro em uma instrução SQL.

## <a name="event-related-errors"></a>Erros relacionados a eventos

O objeto **Error** também é usado quando ocorrem erros relacionados a eventos. Você pode determinar se um erro ocorreu no processo que gerou um evento do ADO verificando o objeto **Error** passado como um parâmetro do evento.

Se a operação que causa um evento é concluída com êxito, o parâmetro *adStatus* do manipulador de eventos será definido como *adStatusOK*. Por outro lado, se a operação que gerou o evento não teve êxito, o parâmetro *adStatus* é definido como *adStatusErrorsOccurred*. Nesse caso, o parâmetro *pError* conterá um objeto **Error** que descreve o erro.

