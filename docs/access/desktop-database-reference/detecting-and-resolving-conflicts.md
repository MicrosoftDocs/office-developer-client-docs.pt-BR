---
title: Detectando e resolvendo conflitos
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c267f33577f3fb2a8d586d33949325517bcc16ba
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944414"
---
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="a559e-102">Detectando e resolvendo conflitos</span><span class="sxs-lookup"><span data-stu-id="a559e-102">Detecting and resolving conflicts</span></span>

<span data-ttu-id="a559e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a559e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="a559e-104">Detecção e solução de conflitos</span><span class="sxs-lookup"><span data-stu-id="a559e-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="a559e-p101">Se você estiver lidando com o **Recordset** no modo imediato, a probabilidade de ocorrerem problemas de simultaneidade é bem menor. Por outro lado, se o aplicativo usar atualização no modo em lotes, é bem provável que um usuário altere um registro antes que as alterações feitas por outro usuário que está editando o mesmo registro sejam salvas. Nesse caso, você desejará que o aplicativo trate o conflito habilmente. Talvez você queira que a última pessoa a enviar uma atualização para o servidor "ganhe". Ou talvez queira permitir que o usuário mais recente decida qual atualização deve prevalecer, permitindo que ele escolha entre os dois valores conflitantes.</span><span class="sxs-lookup"><span data-stu-id="a559e-p101">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise. On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved. In such a case, you will want your application to gracefully handle the conflict. It may be your wish that the last person to send an update to the server "wins." Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="a559e-p102">Seja qual for o caso, o ADO fornece as propriedades **UnderlyingValue** e **OriginalValue** do objeto **Field** para tratar esses tipos de conflitos. Use-as em combinação com o método **Resync** e a propriedade **Filter** do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a559e-p102">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts. Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="a559e-112">Detectando erros</span><span class="sxs-lookup"><span data-stu-id="a559e-112">Detecting Errors</span></span>

<span data-ttu-id="a559e-p103">Quando o ADO encontra um conflito durante uma atualização em lotes, um aviso é colocado na coleção **Errors**. Portanto, você deve sempre verificar se há erros, imediatamente após chamar **BatchUpdate** e, se encontrá-los, comece testando a suposição de que você encontrou um conflito. A primeira etapa é definir a propriedade **Filter** no **Recordset** como **adFilterConflictingRecords** (a propriedade **Filter** é discutida no capítulo anterior). Isso limita a exibição do **Recordset** a apenas aqueles registros que estão em conflito. Se a propriedade **RecordCount** for igual a zero após essa etapa, você saberá que o erro foi causado por outro motivo que não um conflito.</span><span class="sxs-lookup"><span data-stu-id="a559e-p103">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection. Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict. The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter). This limits the view on your **Recordset** to only those records that are in conflict. If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="a559e-p104">Quando você chama **BatchUpdate**, o ADO e o provedor estão gerando instruções SQL para executar atualizações na fonte de dados. Lembre-se de que determinadas fontes de dados têm limitações quanto aos tipos de colunas que podem ser usados em uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="a559e-p104">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source. Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="a559e-120">Em seguida, chame o método **Resync** no **Recordset** com o argumento *AffectRecords* defina igual a **adAffectGroup** e o argumento *ResyncValues* defina igual a **adResyncUnderlyingValues**.</span><span class="sxs-lookup"><span data-stu-id="a559e-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="a559e-121">O método **Resync** atualiza os dados no objeto **Recordset** atual a partir do banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="a559e-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="a559e-122">Usando **adAffectGroup**, você garante que apenas os registros visíveis com a configuração de filtro atual, ou seja, apenas os registros em conflito, sejam resincronizados com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a559e-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="a559e-123">Isso pode fazer uma diferença significativa no desempenho, se você estiver lidando com um **Recordset** grande.</span><span class="sxs-lookup"><span data-stu-id="a559e-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="a559e-124">Definindo o argumento *ResyncValues* como **adResyncUnderlyingValues** quando se chama **Resync**, garantir que a propriedade **UnderlyingValue** conterá o valor (conflitante) do banco de dados, que o **valor** propriedade manterá o valor inserido pelo usuário e que a propriedade **OriginalValue** acomodará o valor original do campo (o valor que tinha antes que a última chamada **UpdateBatch** bem-sucedido foi feita).</span><span class="sxs-lookup"><span data-stu-id="a559e-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="a559e-125">Em seguida, você poderá usar esses valores para resolver o conflito de maneira programática ou deixar que o usuário escolha o valor que será usado.</span><span class="sxs-lookup"><span data-stu-id="a559e-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="a559e-p106">Essa técnica é mostrada no exemplo de código a seguir, o qual cria um conflito artificialmente usando um **Recordset** separado para alterar um valor na tabela de base, antes que **UpdateBatch** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="a559e-p106">This technique is shown in the code example below. The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

<span data-ttu-id="a559e-128">Você pode usar a propriedade **Status** do **Registro** atual ou de um **Campo** específico para determinar o tipo de conflito que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="a559e-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="a559e-129">Para obter informações mais detalhadas sobre o tratamento de erros, consulte [Capítulo 6: Tratamento de erros](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a559e-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

