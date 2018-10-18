---
<span data-ttu-id="2beec-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade ActiveCommand (JScript): ms:assetid de exemplo da propriedade ActiveCommand (JScript): ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: ms.date 48547070: 09/18 / mtps_version 2015: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2beec-101"><<<<<<< HEAD title: ActiveCommand Property Example (JScript) TOCTitle: ActiveCommand Property Example (JScript) ms:assetid: ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: 48547070 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-jscript"></a><span data-ttu-id="2beec-102">Exemplo da propriedade ActiveCommand (JScript)</span><span class="sxs-lookup"><span data-stu-id="2beec-102">ActiveCommand Property Example (JScript)</span></span>

<span data-ttu-id="2beec-103">=== título: exemplo da propriedade ActiveCommand (JScript) TOCTitle: ms:assetid de exemplo (JScript) de propriedade ActiveCommand: ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: ms.date 48547070: 10/17/2018 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="2beec-103">======= title: ActiveCommand property example (JScript) TOCTitle: ActiveCommand property example (JScript) ms:assetid: ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: 48547070 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-jscript"></a><span data-ttu-id="2beec-104">Exemplo da propriedade ActiveCommand (JScript)</span><span class="sxs-lookup"><span data-stu-id="2beec-104">ActiveCommand property example (JScript)</span></span>
>>>>>>> <span data-ttu-id="2beec-105">mestre</span><span class="sxs-lookup"><span data-stu-id="2beec-105">master</span></span>

<span data-ttu-id="2beec-106">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2beec-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2beec-p101">Este exemplo demonstra a propriedade [ActiveCommand](activecommand-property-ado.md). Recorte e cole o código a seguir no Bloco de Notas ou em outro editor de texto e salve-o como **ActiveCommandJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="2beec-p101">This example demonstrates the [ActiveCommand](activecommand-property-ado.md) property. Cut and paste the following code to Notepad or another text editor, and save it as **ActiveCommandJS.asp**.</span></span>

```javascript
<!-- BeginActiveCommandJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<% 
 // user input 
 strName = new String(Request.Form("ContactName")) 
%> 
 
<html> 
 
<head> 
<<<<<<< HEAD
<title>ActiveCommand Property Example (JScript)</title> 
=======
<title>ActiveCommand property example (JScript)</title> 
>>>>>>> master
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="White"> 
 
<<<<<<< HEAD
<h1>ActiveCommand Property Example (JScript)</h1> 
=======
<h1>ActiveCommand property example (JScript)</h1> 
>>>>>>> master
 
<% 
if (strName.length > 0) 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var cmdContact = Server.CreateObject("ADODB.Command"); 
 var rsContact = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 // Open a recordset using a command object 
 cmdContact.CommandText = "SELECT ContactName FROM Customers WHERE City = ?"; 
 cmdContact.ActiveConnection = Cnxn; 
 // create parameter and insert variable value 
 cmdContact.Parameters.Append(cmdContact.CreateParameter("ContactName", adChar, adParamInput, 30, strName)); 
 
 rsContact = cmdContact.Execute(); 
 
 while(!rsContact.EOF){ 
 // start new line 
 strMessage = "<P>"; 
 
 // get data 
 strMessage += rsContact("ContactName") 
 
 // end the line 
 strMessage += "</P>"; 
 
 // show data 
 Response.Write(strMessage); 
 
 // get next record 
 rsContact.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsContact.State == adStateOpen) 
 rsContact.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsContact = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="ActiveCommandJS.asp"> 
 <p align="left">Enter city of customer to find (e.g., Paris): <input type="text" name="ContactName" size="40" value=""></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
</body> 
 
</html> 
<!-- EndActiveCommandJS --> 
 
```

