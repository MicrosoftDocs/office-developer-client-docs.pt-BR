---
title: Exemplo das propriedades ActiveConnection, CommandText e CommandTimeout (JScript)
TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction properties example(JScript)
ms:assetid: 2a79222c-4dba-9c5a-fff7-c8dd2711801f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249056(v=office.15)
ms:contentKeyID: 48543909
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b746902f84aa3afb2213b40d7bab4bb1bc6cb9b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280478"
---
# <a name="activeconnection-commandtext-commandtimeout-commandtype-size-and-direction-properties-example-jscript"></a>Exemplo das propriedades ActiveConnection, CommandText, CommandTimeout, CommandType, Size e Direction (JScript)

**Aplica-se ao:** Access 2013, Office 2013

Este exemplo usa as propriedades [ActiveConnection](activeconnection-property-ado.md), [CommandText](commandtext-property-ado.md), [CommandTimeout](commandtimeout-property-ado.md), [CommandType](commandtype-property-ado.md), [Size](size-property-ado.md) e [Direction](direction-property-ado.md) para executar um procedimento armazenado. Recorte e cole o código a seguir no Bloco de Notas ou em outro editor de texto e salve-o como **ActiveConnectionJS.asp**.

```javascript
<!-- BeginActiveConnectionJS --> 
<%@LANGUAGE="JScript"%> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
<head> 
 <title>ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction Properties</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead { 
 background-color: #008080; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.thead2 { 
 background-color: #800000; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.tbody { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="White"> 
 
<% 
 var iRoyalty = parseInt(Request.Form("RoyaltyValue")); 
 // check user input 
 
 if (iRoyalty > -1) 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var cmdByRoyalty = Server.CreateObject("ADODB.Command"); 
 var rsByRoyalty = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var filter, strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 cmdByRoyalty.CommandText = "byroyalty"; 
 cmdByRoyalty.CommandType = adCmdStoredProc; 
 cmdByRoyalty.CommandTimeOut = 15; 
 
 // The stored procedure called above is as follows: 
 // CREATE PROCEDURE byroyalty 
 // @percentage int 
 // AS 
 // SELECT au_id from titleauthor 
 // WHERE titleauthor.royaltyper = @percentage 
 // GO 
 
 prmByRoyalty = Server.CreateObject("ADODB.Parameter"); 
 prmByRoyalty.Type = adInteger; 
 prmByRoyalty.Size = 3; 
 prmByRoyalty.Direction = adParamInput; 
 prmByRoyalty.Value = iRoyalty; 
 cmdByRoyalty.Parameters.Append(prmByRoyalty); 
 
 cmdByRoyalty.ActiveConnection = Cnxn; 
 
 // recordset by Command - Execute 
 rsByRoyalty = cmdByRoyalty.Execute(); 
 
 // recordset by Recordset - Open 
 rsAuthor.Open("Authors", Cnxn); 
 
 while (!rsByRoyalty.EOF) 
 { 
 // set filter 
 filter = "au_id='" + rsByRoyalty("au_id") 
 rsAuthor.Filter = filter + "'"; 
 
 // start new line 
 strMessage = "<P>"; 
 
 // get data 
 strMessage += rsAuthor("au_fname") + " "; 
 strMessage += rsAuthor("au_lname") + " "; 
 
 // end line 
 strMessage += "</P>"; 
 
 // show data 
 Response.Write(strMessage); 
 
 // get next record 
 rsByRoyalty.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsByRoyalty.State == adStateOpen) 
 rsByRoyalty.Close; 
 if (rsAuthor.State == adStateOpen) 
 rsAuthor.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsByRoyalty = null; 
 rsAuthor = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="ActiveConnectionJS.asp"> 
 <p align="left">Enter royalty percentage to find (e.g., 40): <input type="text" name="RoyaltyValue" size="5"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
&nbsp; 
 
 
</body> 
 
</html> 
<!-- EndActiveConnectionJS --> 
 
```

