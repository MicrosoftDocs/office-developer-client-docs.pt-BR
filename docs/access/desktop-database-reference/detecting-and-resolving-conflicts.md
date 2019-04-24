---
title: Detecção e solução de conflitos
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd7566be2581fe449872eb576bf7f11e5a806fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293921"
---
# <a name="detecting-and-resolving-conflicts"></a>Detecção e solução de conflitos

**Aplica-se ao:** Access 2013, Office 2013

## <a name="detecting-and-resolving-conflicts"></a>Detectando e resolvendo conflitos

Se você estiver lidando com o **Recordset** no modo imediato, a probabilidade de ocorrerem problemas de simultaneidade é bem menor. Por outro lado, se o aplicativo usar atualização no modo em lotes, é bem provável que um usuário altere um registro antes que as alterações feitas por outro usuário que está editando o mesmo registro sejam salvas. Nesse caso, você desejará que o aplicativo trate o conflito habilmente. Talvez você queira que a última pessoa a enviar uma atualização para o servidor "ganhe". Ou talvez queira permitir que o usuário mais recente decida qual atualização deve prevalecer, permitindo que ele escolha entre os dois valores conflitantes.

Seja qual for o caso, o ADO fornece as propriedades **UnderlyingValue** e **OriginalValue** do objeto **Field** para tratar esses tipos de conflitos. Use-as em combinação com o método **Resync** e a propriedade **Filter** do **Recordset**.

## <a name="detecting-errors"></a>Detectando erros

Quando o ADO encontra um conflito durante uma atualização em lotes, um aviso é colocado na coleção **Errors**. Portanto, você deve sempre verificar se há erros, imediatamente após chamar **BatchUpdate** e, se encontrá-los, comece testando a suposição de que você encontrou um conflito. A primeira etapa é definir a propriedade **Filter** no **Recordset** como **adFilterConflictingRecords** (a propriedade **Filter** é discutida no capítulo anterior). Isso limita a exibição do **Recordset** a apenas aqueles registros que estão em conflito. Se a propriedade **RecordCount** for igual a zero após essa etapa, você saberá que o erro foi causado por outro motivo que não um conflito.

Quando você chama **BatchUpdate**, o ADO e o provedor estão gerando instruções SQL para executar atualizações na fonte de dados. Lembre-se de que determinadas fontes de dados têm limitações quanto aos tipos de colunas que podem ser usados em uma cláusula WHERE.

Em seguida, chame o método **Resync** no **Recordset** com o argumento *AffectRecords* definido como **adAffectGroup** e o argumento *ResyncValues* definido como **adResyncUnderlyingValues**. O método **Resync** atualiza os dados no objeto **Recordset** atual a partir do banco de dados subjacente. Usando **adAffectGroup**, você garante que apenas os registros visíveis com a configuração de filtro atual, ou seja, apenas os registros em conflito, sejam resincronizados com o banco de dados. Isso pode fazer uma diferença significativa no desempenho, se você estiver lidando com um **Recordset** grande. Definindo o argumento *ResyncValues* como **adResyncUnderlyingValues** ao chamar **Resync**, você garante que a propriedade **UnderlyingValue** conterá o valor (conflitante) do banco de dados, que a propriedade **Value** manterá o valor inserido pelo usuário e que a propriedade **OriginalValue** manterá o valor original do campo (o valor que ele tinha antes que a última chamada bem-sucedida para **UpdateBatch** fosse feita). Em seguida, você poderá usar esses valores para resolver o conflito de maneira programática ou deixar que o usuário escolha o valor que será usado.

Essa técnica é mostrada no exemplo de código a seguir, o qual cria um conflito artificialmente usando um **Recordset** separado para alterar um valor na tabela de base, antes que **UpdateBatch** seja chamado.

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

Você pode usar a propriedade **Status** do **Registro** atual ou de um **Campo** específico para determinar o tipo de conflito que ocorreu.

Para obter informações mais detalhadas sobre o tratamento de erros, consulte [Capítulo 6: Tratamento de erros](chapter-6-error-handling.md).

