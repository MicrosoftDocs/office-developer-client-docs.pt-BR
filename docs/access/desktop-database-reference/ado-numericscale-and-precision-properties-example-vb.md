---
<span data-ttu-id="75c41-101"><<<<<<< Título cabeça: ADO NumericScale e Precision propriedades exemplo (VB) TOCTitle: NumericScale e Precision propriedades exemplo (VB) === título: exemplo das propriedades ADO NumericScale e Precision (VB) TOCTitle: NumericScale e Exemplo das propriedades Precision (VB)</span><span class="sxs-lookup"><span data-stu-id="75c41-101"><<<<<<< HEAD title: ADO NumericScale and Precision Properties Example (VB) TOCTitle: NumericScale and Precision Properties Example (VB) ======= title: ADO NumericScale and Precision properties example (VB) TOCTitle: NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="75c41-102">ms:assetid de mestre: 060394b1-0c2c-3726-92a0-0f350bbaa3d5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15) ms:contentKeyID: ms.date 48543044: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="75c41-102">master ms:assetid: 060394b1-0c2c-3726-92a0-0f350bbaa3d5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15) ms:contentKeyID: 48543044 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="75c41-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="75c41-103"><<<<<<< HEAD</span></span>
# <a name="ado-numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="75c41-104">ADO exemplo NumericScale e Precision propriedades (VB)</span><span class="sxs-lookup"><span data-stu-id="75c41-104">ADO NumericScale and Precision Properties Example (VB)</span></span>
=======
# <a name="ado-numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="75c41-105">Exemplo das propriedades ADO NumericScale e Precision (VB)</span><span class="sxs-lookup"><span data-stu-id="75c41-105">ADO NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="75c41-106">mestre</span><span class="sxs-lookup"><span data-stu-id="75c41-106">master</span></span>


<span data-ttu-id="75c41-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75c41-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75c41-108">Este exemplo usa as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md) para exibir a escala numérica e a precisão de campos na tabela ***Discounts*** do banco de dados ***Pubs***.</span><span class="sxs-lookup"><span data-stu-id="75c41-108">This example uses the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties to display the numeric scale and precision of fields in the ***Discounts*** table of the ***Pubs*** database.</span></span>

```vb 
 
'BeginNumericScaleVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim rstDiscounts As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim fldTemp As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLDiscounts As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset 
 Set rstDiscounts = New ADODB.Recordset 
 strSQLDiscounts = "Discounts" 
 rstDiscounts.Open strSQLDiscounts, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 
 ' Display numeric scale and precision of 
 ' numeric and small integer fields 
 For Each fldTemp In rstDiscounts.Fields 
 If fldTemp.Type = adNumeric Or fldTemp.Type = adSmallInt Then 
 MsgBox "Field: " & fldTemp.Name & vbCr & _ 
 "Numeric scale: " & _ 
 fldTemp.NumericScale & vbCr & _ 
 "Precision: " & fldTemp.Precision 
 End If 
 Next fldTemp 
 
 ' clean up 
 rstDiscounts.Close 
 Cnxn.Close 
 Set rstDiscounts = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstDiscounts Is Nothing Then 
 If rstDiscounts.State = adStateOpen Then rstDiscounts.Close 
 End If 
 Set rstDiscounts = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndNumericScaleVB 
```

