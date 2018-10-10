---
title: Exemplo da propriedade Type (Property) (VB)
TOCTitle: Type Property Example (Property) (VB)
ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15)
ms:contentKeyID: 48547209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b99729b4826f25aa8b5f32475ad4b3f0921e849
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463075"
---
# <a name="type-property-example-property-vb"></a><span data-ttu-id="7f79a-102">Exemplo da propriedade Type (Property) (VB)</span><span class="sxs-lookup"><span data-stu-id="7f79a-102">Type Property Example (Property) (VB)</span></span>


<span data-ttu-id="7f79a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f79a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f79a-p101">Este exemplo demonstra a propriedade [Type](type-property-ado.md). É o modelo de um utilitário para relacionar nomes e tipos de uma coleção, como [Properties](properties-collection-ado.md), [Fields](fields-collection-ado.md), etc.</span><span class="sxs-lookup"><span data-stu-id="7f79a-p101">This example demonstrates the [Type](type-property-ado.md) property. It is a model of a utility for listing the names and types of a collection, like [Properties](properties-collection-ado.md), [Fields](fields-collection-ado.md), etc.</span></span>

<span data-ttu-id="7f79a-p102">Não é necessário abrir o [Recordset](recordset-object-ado.md) para acessar sua coleção **Properties**; ela é exibida quando uma instância do objeto **Recordset** é criada. Entretanto, ao definir a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient** são adicionadas várias propriedades dinâmicas à coleção **Properties** do objeto **Recordset**, tornando o exemplo um pouco mais interessante. Como ilustração, utilizamos explicitamente a propriedade [Item](item-property-ado.md) para acessar cada objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7f79a-p102">We do not need to open the [Recordset](recordset-object-ado.md) to access its **Properties** collection; they come into existence when the **Recordset** object is instantiated. However, setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** adds several dynamic properties to the **Recordset** object's **Properties** collection, making the example a little more interesting. For sake of illustration, we explicitly use the [Item](item-property-ado.md) property to access each [Property](property-object-ado.md) object.</span></span>

```vb 
 
'BeginTypePropertyVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rst As ADODB.Recordset 
 Dim prop As ADODB.Property 
 ' property variables 
 Dim ix As Integer 
 Dim strMsg As String 
 
 ' create client-side recordset 
 Set rst = New ADODB.Recordset 
 rst.CursorLocation = adUseClient 
 ' enumerate property types 
 For ix = 0 To rst.Properties.Count - 1 
 Set prop = rst.Properties.Item(ix) 
 Select Case prop.Type 
 Case adBigInt 
 strMsg = "adBigInt" 
 Case adBinary 
 strMsg = "adBinary" 
 Case adBoolean 
 strMsg = "adBoolean" 
 Case adBSTR 
 strMsg = "adBSTR" 
 Case adChapter 
 strMsg = "adChapter" 
 Case adChar 
 strMsg = "adChar" 
 Case adCurrency 
 strMsg = "adCurrency" 
 Case adDate 
 strMsg = "adDate" 
 Case adDBDate 
 strMsg = "adDBDate" 
 Case adDBTime 
 strMsg = "adDBTime" 
 Case adDBTimeStamp 
 strMsg = "adDBTimeStamp" 
 Case adDecimal 
 strMsg = "adDecimal" 
 Case adDouble 
 strMsg = "adDouble" 
 Case adEmpty 
 strMsg = "adEmpty" 
 Case adError 
 strMsg = "adError" 
 Case adFileTime 
 strMsg = "adFileTime" 
 Case adGUID 
 strMsg = "adGUID" 
 Case adIDispatch 
 strMsg = "adIDispatch" 
 Case adInteger 
 strMsg = "adInteger" 
 Case adIUnknown 
 strMsg = "adIUnknown" 
 Case adLongVarBinary 
 strMsg = "adLongVarBinary" 
 Case adLongVarChar 
 strMsg = "adLongVarChar" 
 Case adLongVarWChar 
 strMsg = "adLongVarWChar" 
 Case adNumeric 
 strMsg = "adNumeric" 
 Case adPropVariant 
 strMsg = "adPropVariant" 
 Case adSingle 
 strMsg = "adSingle" 
 Case adSmallInt 
 strMsg = "adSmallInt" 
 Case adTinyInt 
 strMsg = "adTinyInt" 
 Case adUnsignedBigInt 
 strMsg = "adUnsignedBigInt" 
 Case adUnsignedInt 
 strMsg = "adUnsignedInt" 
 Case adUnsignedSmallInt 
 strMsg = "adUnsignedSmallInt" 
 Case adUnsignedTinyInt 
 strMsg = "adUnsignedTinyInt" 
 Case adUserDefined 
 strMsg = "adUserDefined" 
 Case adVarBinary 
 strMsg = "adVarBinary" 
 Case adVarChar 
 strMsg = "adVarChar" 
 Case adVariant 
 strMsg = "adVariant" 
 Case adVarNumeric 
 strMsg = "adVarNumeric" 
 Case adVarWChar 
 strMsg = "adVarWChar" 
 Case adWChar 
 strMsg = "adWChar" 
 Case Else 
 strMsg = "*UNKNOWN*" 
 End Select 
 'show results 
 Debug.Print "Property " & ix & ": " & prop.Name & _ 
 ", Type = " & strMsg 
 Next ix 
 
 ' clean up 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndTypePropertyVB 
```

