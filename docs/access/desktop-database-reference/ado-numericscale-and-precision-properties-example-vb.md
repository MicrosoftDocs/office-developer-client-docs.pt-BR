---
title: ADO exemplo NumericScale e Precision propriedades (VB)
TOCTitle: NumericScale and Precision Properties Example (VB)
ms:assetid: 060394b1-0c2c-3726-92a0-0f350bbaa3d5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15)
ms:contentKeyID: 48543044
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 773363b968f592bc8773f498db0d4114ad16c41b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462255"
---
# <a name="ado-numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="b95e6-102">ADO exemplo NumericScale e Precision propriedades (VB)</span><span class="sxs-lookup"><span data-stu-id="b95e6-102">ADO NumericScale and Precision Properties Example (VB)</span></span>


<span data-ttu-id="b95e6-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b95e6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b95e6-104">Este exemplo usa as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md) para exibir a escala numérica e a precisão de campos na tabela ***Discounts*** do banco de dados ***Pubs***.</span><span class="sxs-lookup"><span data-stu-id="b95e6-104">This example uses the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties to display the numeric scale and precision of fields in the ***Discounts*** table of the ***Pubs*** database.</span></span>

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

