---
<span data-ttu-id="3759e-101"><<<<<<< Título cabeça: Description, HelpContext, HelpFile propriedades exemplo (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, número, fonte e exemplo de propriedades SQLState (VB) === título: descrição, HelpContext, HelpFile exemplo das propriedades (VB) TOCTitle: exemplo das propriedades Description, HelpContext, HelpFile, NativeError, número, Source e SQLState (VB)</span><span class="sxs-lookup"><span data-stu-id="3759e-101"><<<<<<< HEAD title: Description, HelpContext, HelpFile Properties Example (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB) ======= title: Description, HelpContext, HelpFile properties example (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="3759e-102">ms:assetid de mestre: 3c129aec-cd69-5822-4dad-ebef226538e1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) ms:contentKeyID: ms.date 48544304: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3759e-102">master ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) ms:contentKeyID: 48544304 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3759e-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="3759e-103"><<<<<<< HEAD</span></span>
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="3759e-104">Exemplo das propriedades Description, HelpContext, HelpFile, NativeError, Number, Source e SQLState (VB)</span><span class="sxs-lookup"><span data-stu-id="3759e-104">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB)</span></span>
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="3759e-105">Exemplo das propriedades Description, HelpContext, HelpFile, NativeError, número, Source e SQLState (VB)</span><span class="sxs-lookup"><span data-stu-id="3759e-105">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="3759e-106">mestre</span><span class="sxs-lookup"><span data-stu-id="3759e-106">master</span></span>


<span data-ttu-id="3759e-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3759e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3759e-108">Este exemplo dispara um erro, intercepta-o e exibe as propriedades [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md) e [SQLState](sqlstate-property-ado.md) do objeto [Error](error-object-ado.md) resultante.</span><span class="sxs-lookup"><span data-stu-id="3759e-108">This example triggers an error, traps it, and displays the [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md), and [SQLState](sqlstate-property-ado.md) properties of the resulting [Error](error-object-ado.md) object.</span></span>

```vb
    'BeginDescriptionVB
    Public Sub Main()
    
        Dim Cnxn As ADODB.Connection
        Dim Err As ADODB.Error
        Dim strError As String
        
        On Error GoTo ErrorHandler
        
        ' Intentionally trigger an error
        Set Cnxn = New ADODB.Connection
        Cnxn.Open "nothing"
        
        Set Cnxn = Nothing
        Exit Sub
    
    ErrorHandler:
    
        ' Enumerate Errors collection and display
        ' properties of each Error object
        For Each Err In Cnxn.Errors
            strError = "Error #" & Err.Number & vbCr & _
                "   " & Err.Description & vbCr & _
                "   (Source: " & Err.Source & ")" & vbCr & _
                "   (SQL State: " & Err.SQLState & ")" & vbCr & _
                "   (NativeError: " & Err.NativeError & ")" & vbCr
            If Err.HelpFile = "" Then
                strError = strError & "   No Help file available"
            Else
                strError = strError & _
                   "   (HelpFile: " & Err.HelpFile & ")" & vbCr & _
                   "   (HelpContext: " & Err.HelpContext & ")" & _
                   vbCr & vbCr
            End If
             
            Debug.Print strError
        Next
    
        Resume Next
    End Sub
    'EndDescriptionVB
```
