---
title: Parâmetros de evento (referência de banco de dados da área de trabalho do Access)
TOCTitle: Event Parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 023109586d13dc25846c8c145746aaf97fc22c15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888367"
---
# <a name="event-parameters"></a>Parâmetros de eventos


**Aplica-se a**: Access 2013, o Office 2013


Cada manipulador de eventos possui um parâmetro de status que o controla. No caso dos eventos Complete, esse parâmetro também é usado para indicar o êxito ou a falha da operação que gerou o evento. A maioria desses eventos também possui um parâmetro de erro que fornece informações sobre qualquer erro que possa ter ocorrido, bem como um ou mais parâmetros de objeto que fazem referência aos objetos ADO usados para executar a operação. Por exemplo o evento [ExecuteComplete](executecomplete-event-ado.md) inclui parâmetros para os objetos **Command**, **Recordset** e **Connection** associados ao evento. Neste exemplo do Microsoft Visual Basic, você poderá ver os objetos pCommand, pRecordset e pConnection que representam os objetos **Command**, **Recordset** e **Connection** usados pelo método **Execute**.

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

Os mesmos parâmetros são passados para os eventos Will, com exceção do objeto **Error**. Desse modo, você terá a oportunidade de examinar cada um dos objetos a serem usados na operação pendente e determinar se a operação deverá obter permissão para ser concluída.

Alguns manipuladores de eventos possuem o parâmetro *Reason*, que fornece informações adicionais sobre o motivo do evento. Por exemplo, os eventos **WillMove** e **MoveComplete** podem ocorrer devido à chamada de qualquer um dos métodos de navegação (**MoveNext**, **MovePrevious** etc.) ou como resultado de uma repetição de consulta.

## <a name="status-parameter"></a>Parâmetro Status

Quando a rotina manipuladora de eventos é chamada, o parâmetro *Status* é definido para um destes valores.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>Passado para os eventos Will e Complete. Este valor indica que a operação que causou o evento foi concluída com êxito.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Passado somente para os eventos Complete. Este valor indica que a operação que causou o evento não teve êxito ou que um evento Will cancelou a operação. Verifique o parâmetro <em>Error</em> para obter mais detalhes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Passado somente para os eventos Will. Este valor indica que a operação não pode ser cancelada pelo evento Will e deve ser executada.</p></td>
</tr>
</tbody>
</table>


Se você determinar em seu evento Will que a operação deve continuar, não altere o parâmetro *Status*. Entretanto, se o parâmetro de status de entrada não estiver definido como **adStatusCantDeny**, você poderá cancelar a operação pendente, alterando *Status* para **adStatusCancel**. Em seguida, o evento Complete associado à operação terá seu parâmetro *Status* definido como **adStatusErrorsOccurred**. O objeto **Error** passado para o evento Complete conterá o valor **adErrOperationCancelled**.

Se não desejar mais processar um evento, você poderá definir *Status* como **adStatusUnwantedEvent** para que seu aplicativo não receba mais notificações desse evento. Lembre-se, entretanto, de que alguns eventos podem ser gerados por mais de um motivo. Nesse caso, você deve especificar **adStatusUnwantedEvent** para cada motivo possível. Por exemplo, para interromper o recebimento de notificação de eventos **RecordChange** pendentes, defina o parâmetro *Status* como **adStatusUnwantedEvent** para **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** e **adRsnFirstChange** à medida que eles ocorrerem.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>Solicita que o manipulador de eventos não receba mais notificações.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Solicita o cancelamento da operação que está prestes a ocorrer.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Parâmetro Error

O parâmetro *Error* for uma referência a um objeto ADO [erro](error-object-ado.md) . Quando o parâmetro *Status* é definido como **adStatusErrorsOccurred**, o objeto **Error** contém detalhes sobre por que a operação falhou. Se o evento será associado a um evento Complete cancelou a operação, definindo o parâmetro *Status* como **adStatusCancel**, o objeto error sempre é definido como **adErrOperationCancelled**.

## <a name="object-parameter"></a>Parâmetro Object

Cada evento recebe um ou mais objetos que representam os objetos envolvidos na operação. Por exemplo, o evento **ExecuteComplete** recebe um objeto **Command**, um objeto **Recordset** e um objeto **Connection**.

## <a name="reason-parameter"></a>Parâmetro Reason

O parâmetro *Reason*, *adReason*, fornece informações adicionais sobre o motivo do evento. Os eventos com esse tipo de parâmetro podem ser chamados várias vezes, inclusive para a mesma operação, e sempre por um motivo diferente. Por exemplo, o manipulador de eventos ****WillChangeRecord** é chamado para as operações que estão prestes a fazer ou desfazer a inserção, a exclusão ou a modificação de um registro. Se desejar processar somente um evento no momento em que ele ocorrer por um determinado motivo, você poderá usar o parâmetro *adReason* para filtrar as ocorrências que não sejam de seu interesse. Por exemplo, se desejar processar somente eventos de alteração de registro quando eles ocorrerem devido à adição de um registro, você poderá executar este procedimento:

```vb 
 
' BeginEventExampleVB01 
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset) 
 If adReason = adRsnAddNew Then 
 ' Process event 
 '... 
 Else 
 ' Cancel event notification for all 
 ' other possible adReason values. 
 adStatus = adStatusUnwantedEvent 
 End If 
End Sub 
' EndEventExampleVB01 
```

Neste caso, a notificação poderá ocorrer para cada um dos outros motivos. Entretanto, ela ocorrerá apenas uma vez para cada um deles. Depois que ela ocorrer uma vez para cada motivo, você somente a receberá caso adicione um novo registro.

Por outro lado, você precisará definir *adStatus* como **adStatusUnwantedEvent somente uma vez para solicitar que um manipulador de eventos sem o parâmetro **adReason** pare de receber notificações de evento** .

