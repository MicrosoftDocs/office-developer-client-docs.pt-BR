---
title: Exemplo do método AddNew (JScript)
TOCTitle: AddNew Method Example (JScript)
ms:assetid: b6f7e98d-d34d-dc2a-bdcb-65452f3fe5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249882(v=office.15)
ms:contentKeyID: 48547290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 203930b24f49af82771206024369c79cfa24f8b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464304"
---
# <a name="addnew-method-example-jscript"></a>Exemplo do método AddNew (JScript)

**Aplica-se a**: Access 2013 | Office 2013

Este exemplo utiliza o método [AddNew](addnew-method-ado.md) para criar um novo registro com o nome especificado. Recorte e cole o código a seguir no Bloco de notas ou em outro editor de texto e salve-o como **AddNewJS.asp**.

```javascript
<!-- BeginAddNewJS --> 
<%@LANGUAGE="JScript" %> 
<!-- Include file for JScript ADO Constants --> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
 <title>Add New Method Example (JScript)</title> 
<style> 
<!-- 
body { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body> 
<h1>AddNew Method Example (JScript)</h1> 
 
<% 
 if (Request.Form("Addit") == "AddNew") 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 //record variables 
 var FName = String(Request.Form("FirstName")); 
 var LName = String(Request.Form("LastName")); 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn) 
 
 // open Employee recordset using client-side cursor 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("Employees", strCnxn, adOpenKeyset, adLockOptimistic, adCmdTable); 
 
 rsEmployee.AddNew(); 
 rsEmployee("FirstName") = FName; 
 rsEmployee("LastName") = LName; 
 rsEmployee.Update; 
 
 // of course, you would normally do error handling here 
 Response.Write("New record added.") 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsEmployee = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<form method="post" action="AddNewJS.asp" id=form1 name=form1> 
<table> 
<tr> 
 <td colspan="2"> 
 <h4>Please enter the record to add:</h4> 
 </td> 
</tr> 
<tr> 
 <td> 
 First Name: 
 </td> 
 <td> 
 <input name="FirstName" maxLength=20> 
 </td> 
</tr> 
<tr> 
 <td> 
 Last Name: 
 </td> 
 <td> 
 <input name="LastName" size="30" maxLength=30> 
 </td> 
</tr> 
<tr> 
 <td align="right"> 
 <input type="submit" value="Submit" name="Submit"> 
 </td> 
 <TD align="left"> 
 <INPUT type="reset" value="Reset" name="Reset"> 
 </TD> 
</tr> 
</table> 

<INPUT type="hidden" value="AddNew" name="Addit"> 
</form> 
</body> 
</HTML> 
<!-- EndAddNewJS --> 
 
```
