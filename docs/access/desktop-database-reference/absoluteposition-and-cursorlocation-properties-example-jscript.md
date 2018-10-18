---
<<<<<<< Título cabeça: AbsolutePosition e CursorLocation exemplo das propriedades (JScript) TOCTitle: AbsolutePosition e CursorLocation exemplo das propriedades (JScript) ms:assetid: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID: ms.date 48548142: 18/09/2015 mtps_version: v=office.15
---

# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a>Exemplo das propriedades AbsolutePosition e CursorLocation (JScript)

=== título: exemplo das propriedades AbsolutePosition e CursorLocation (JScript) TOCTitle: ms:assetid de exemplo (JScript) propriedades AbsolutePosition e CursorLocation: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID: ms.date 48548142: 10/17/2018 mtps_version: v=office.15
---

# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a>Exemplo das propriedades AbsolutePosition e CursorLocation (JScript)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Este exemplo demonstra como a propriedade [AbsolutePosition](absoluteposition-property-ado.md) pode rastrear o progresso de um loop que enumera todos os registros de um [Recordset](recordset-object-ado.md). A propriedade [CursorLocation](cursorlocation-property-ado.md) é utilizada para habilitar a propriedade **AbsolutePosition**, definindo o cursor como um cliente. Recorte e cole o código a seguir no Bloco de Notas ou em outro editor de texto e salve-o como **AbsolutePositionJS.asp**.

```javascript
<!-- BeginAbsolutePositionJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<<<<<<< HEAD
<title>AbsolutePosition and CursorLocation Properties Example (JScript)</title> 
=======
<title>AbsolutePosition and CursorLocation properties example (JScript)</title> 
>>>>>>> master
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
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
 
<body> 
<<<<<<< HEAD
<h1>AbsolutePosition and CursorLocation Properties Example (JScript)</h1> 
=======
<h1>AbsolutePosition and CursorLocation properties example (JScript)</h1> 
>>>>>>> master
<% 
 // connection and recordset variables 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 // display string 
 var strMessage; 
 
 try 
 { 
 // Open a recordset on the Employee table using 
 // a client-side cursor to enable AbsolutePosition property. 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("employees", strCnxn, adOpenStatic, adLockOptimistic, adCmdTable); 
 
 // Write beginning of table to the document. 
 Response.Write('<table border="0" align="center">'); 
 Response.Write('<tr class="thead2">'); 
 Response.Write("<th>AbsolutePosition</th><th>Name</th><th>Hire Date</th></tr>"); 
 
 while (!rsEmployee.EOF) 
 { 
 strMessage = ""; 
 
 // Start a new table row. 
 strMessage = '<tr class="tbody">'; 
 
 // First column in row contains AbsolutePosition value. 
 strMessage += "<td>" + rsEmployee.AbsolutePosition + " of " + rsEmployee.RecordCount + "</td>" 
 
 // First and last name are in first column. 
 strMessage += "<td>" + rsEmployee.Fields("FirstName") + " "; 
 strMessage += rsEmployee.Fields("LastName") + " " + "</td>"; 
 
 // Hire date in second column. 
 strMessage += "<td>" + rsEmployee.Fields("HireDate") + "</td>"; 
 
 // End the row. 
 strMessage += "</tr>"; 
 
 // Write line to document. 
 Response.Write(strMessage); 
 
 // Get next record. 
 rsEmployee.MoveNext; 
 } 
 
 // Finish writing document. 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 rsEmployee = null; 
 } 
%> 
 
</html> 
<!-- EndAbsolutePositionJS --> 
```

