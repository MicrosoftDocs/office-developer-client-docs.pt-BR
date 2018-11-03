---
title: Parâmetros de evento (referência de banco de dados da área de trabalho do Access)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3acad111c3e1329f50c64f3f6fd6c5f7430e558d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946738"
---
# <a name="event-parameters"></a><span data-ttu-id="adc59-102">Parâmetros de evento</span><span class="sxs-lookup"><span data-stu-id="adc59-102">Event parameters</span></span>

<span data-ttu-id="adc59-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="adc59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adc59-p101">Cada manipulador de eventos possui um parâmetro de status que o controla. No caso dos eventos Complete, esse parâmetro também é usado para indicar o êxito ou a falha da operação que gerou o evento. A maioria desses eventos também possui um parâmetro de erro que fornece informações sobre qualquer erro que possa ter ocorrido, bem como um ou mais parâmetros de objeto que fazem referência aos objetos ADO usados para executar a operação. Por exemplo o evento [ExecuteComplete](executecomplete-event-ado.md) inclui parâmetros para os objetos **Command**, **Recordset** e **Connection** associados ao evento. Neste exemplo do Microsoft Visual Basic, você poderá ver os objetos pCommand, pRecordset e pConnection que representam os objetos **Command**, **Recordset** e **Connection** usados pelo método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="adc59-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="adc59-p102">Os mesmos parâmetros são passados para os eventos Will, com exceção do objeto **Error**. Desse modo, você terá a oportunidade de examinar cada um dos objetos a serem usados na operação pendente e determinar se a operação deverá obter permissão para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="adc59-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="adc59-p103">Alguns manipuladores de eventos possuem o parâmetro *Reason*, que fornece informações adicionais sobre o motivo do evento. Por exemplo, os eventos **WillMove** e **MoveComplete** podem ocorrer devido à chamada de qualquer um dos métodos de navegação (**MoveNext**, **MovePrevious** etc.) ou como resultado de uma repetição de consulta.</span><span class="sxs-lookup"><span data-stu-id="adc59-p103">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred. For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="adc59-113">Parâmetro Status</span><span class="sxs-lookup"><span data-stu-id="adc59-113">Status Parameter</span></span>

<span data-ttu-id="adc59-114">Quando a rotina manipuladora de eventos é chamada, o parâmetro *Status* é definido para um destes valores.</span><span class="sxs-lookup"><span data-stu-id="adc59-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adc59-115">Valor</span><span class="sxs-lookup"><span data-stu-id="adc59-115">Value</span></span></p></th>
<th><p><span data-ttu-id="adc59-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="adc59-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adc59-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="adc59-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="adc59-p104">Passado para os eventos Will e Complete. Este valor indica que a operação que causou o evento foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="adc59-p104">Passed to both Will and Complete events. This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adc59-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="adc59-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="adc59-p105">Passado somente para os eventos Complete. Este valor indica que a operação que causou o evento não teve êxito ou que um evento Will cancelou a operação. Verifique o parâmetro <em>Error</em> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="adc59-p105">Passed to Complete events only. This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation. Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adc59-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="adc59-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="adc59-p106">Passado somente para os eventos Will. Este valor indica que a operação não pode ser cancelada pelo evento Will e deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="adc59-p106">Passed to Will events only. This value means that the operation cannot be canceled by the Will event. It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adc59-p107">Se você determinar em seu evento Will que a operação deve continuar, não altere o parâmetro *Status*. Entretanto, se o parâmetro de status de entrada não estiver definido como **adStatusCantDeny**, você poderá cancelar a operação pendente, alterando *Status* para **adStatusCancel**. Em seguida, o evento Complete associado à operação terá seu parâmetro *Status* definido como **adStatusErrorsOccurred**. O objeto **Error** passado para o evento Complete conterá o valor **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="adc59-p107">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged. As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**. When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**. The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="adc59-p108">Se não desejar mais processar um evento, você poderá definir *Status* como **adStatusUnwantedEvent** para que seu aplicativo não receba mais notificações desse evento. Lembre-se, entretanto, de que alguns eventos podem ser gerados por mais de um motivo. Nesse caso, você deve especificar **adStatusUnwantedEvent** para cada motivo possível. Por exemplo, para interromper o recebimento de notificação de eventos **RecordChange** pendentes, defina o parâmetro *Status* como **adStatusUnwantedEvent** para **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** e **adRsnFirstChange** à medida que eles ocorrerem.</span><span class="sxs-lookup"><span data-stu-id="adc59-p108">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event. Remember, however, that some events can be raised for more than one reason. In that case, you must specify **adStatusUnwantedEvent** for each possible reason. For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adc59-136">Valor</span><span class="sxs-lookup"><span data-stu-id="adc59-136">Value</span></span></p></th>
<th><p><span data-ttu-id="adc59-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="adc59-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adc59-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="adc59-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="adc59-139">Solicita que o manipulador de eventos não receba mais notificações.</span><span class="sxs-lookup"><span data-stu-id="adc59-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adc59-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="adc59-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="adc59-141">Solicita o cancelamento da operação que está prestes a ocorrer.</span><span class="sxs-lookup"><span data-stu-id="adc59-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="adc59-142">Parâmetro Error</span><span class="sxs-lookup"><span data-stu-id="adc59-142">Error Parameter</span></span>

<span data-ttu-id="adc59-143">O parâmetro *Error* for uma referência a um objeto ADO [erro](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="adc59-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="adc59-144">Quando o parâmetro *Status* é definido como **adStatusErrorsOccurred**, o objeto **Error** contém detalhes sobre por que a operação falhou.</span><span class="sxs-lookup"><span data-stu-id="adc59-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="adc59-145">Se o evento será associado a um evento Complete cancelou a operação, definindo o parâmetro *Status* como **adStatusCancel**, o objeto error sempre é definido como **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="adc59-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="adc59-146">Parâmetro Object</span><span class="sxs-lookup"><span data-stu-id="adc59-146">Object Parameter</span></span>

<span data-ttu-id="adc59-p110">Cada evento recebe um ou mais objetos que representam os objetos envolvidos na operação. Por exemplo, o evento **ExecuteComplete** recebe um objeto **Command**, um objeto **Recordset** e um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="adc59-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="adc59-149">Parâmetro Reason</span><span class="sxs-lookup"><span data-stu-id="adc59-149">Reason Parameter</span></span>

<span data-ttu-id="adc59-p111">O parâmetro *Reason*, *adReason*, fornece informações adicionais sobre o motivo do evento. Os eventos com esse tipo de parâmetro podem ser chamados várias vezes, inclusive para a mesma operação, e sempre por um motivo diferente. Por exemplo, o manipulador de eventos \*\*\*\*WillChangeRecord\*\* é chamado para as operações que estão prestes a fazer ou desfazer a inserção, a exclusão ou a modificação de um registro. Se desejar processar somente um evento no momento em que ele ocorrer por um determinado motivo, você poderá usar o parâmetro *adReason* para filtrar as ocorrências que não sejam de seu interesse. Por exemplo, se desejar processar somente eventos de alteração de registro quando eles ocorrerem devido à adição de um registro, você poderá executar este procedimento:</span><span class="sxs-lookup"><span data-stu-id="adc59-p111">The *Reason* parameter, *adReason*, provides additional information about why the event occurred. Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason. For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record. If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in. For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="adc59-p112">Neste caso, a notificação poderá ocorrer para cada um dos outros motivos. Entretanto, ela ocorrerá apenas uma vez para cada um deles. Depois que ela ocorrer uma vez para cada motivo, você somente a receberá caso adicione um novo registro.</span><span class="sxs-lookup"><span data-stu-id="adc59-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="adc59-158">Por outro lado, você precisará definir *adStatus* como **adStatusUnwantedEvent somente uma vez para solicitar que um manipulador de eventos sem o parâmetro **adReason** pare de receber notificações de evento** .</span><span class="sxs-lookup"><span data-stu-id="adc59-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

