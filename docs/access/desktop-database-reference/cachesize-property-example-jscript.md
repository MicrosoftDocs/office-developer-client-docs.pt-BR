---
<span data-ttu-id="2f40f-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade CacheSize (JScript): exemplo da propriedade CacheSize (JScript) === título: exemplo da propriedade CacheSize (JScript) TOCTitle: exemplo da propriedade CacheSize (JScript)</span><span class="sxs-lookup"><span data-stu-id="2f40f-101"><<<<<<< HEAD title: CacheSize Property Example (JScript) TOCTitle: CacheSize Property Example (JScript) ======= title: CacheSize property example (JScript) TOCTitle: CacheSize property example (JScript)</span></span>
>>>>>>> <span data-ttu-id="2f40f-102">ms:assetid de mestre: bee835cb-8d26-b8b7-4958-39261809b86c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249928(v=office.15) ms:contentKeyID: ms.date 48547473: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2f40f-102">master ms:assetid: bee835cb-8d26-b8b7-4958-39261809b86c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249928(v=office.15) ms:contentKeyID: 48547473 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2f40f-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="2f40f-103"><<<<<<< HEAD</span></span>
# <a name="cachesize-property-example-jscript"></a><span data-ttu-id="2f40f-104">Exemplo da propriedade CacheSize (JScript)</span><span class="sxs-lookup"><span data-stu-id="2f40f-104">CacheSize Property Example (JScript)</span></span>
=======
# <a name="cachesize-property-example-jscript"></a><span data-ttu-id="2f40f-105">Exemplo da propriedade CacheSize (JScript)</span><span class="sxs-lookup"><span data-stu-id="2f40f-105">CacheSize property example (JScript)</span></span>
>>>>>>> <span data-ttu-id="2f40f-106">mestre</span><span class="sxs-lookup"><span data-stu-id="2f40f-106">master</span></span>


<span data-ttu-id="2f40f-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f40f-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f40f-p101">Este exemplo usa a propriedade [CacheSize](cachesize-property-ado.md) para mostrar a diferença no desempenho de uma operação realizada com e sem um cache de 30 registros. Recorte e cole o código a seguir no Bloco de Notas ou em outro editor de texto e salve-o como **CacheSizeJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="2f40f-p101">This example uses the [CacheSize](cachesize-property-ado.md) property to show the difference in performance for an operation performed with and without a 30-record cache. Cut and paste the following code to Notepad or another text editor, and save it as **CacheSizeJS.asp**.</span></span>

```javascript 
 
<!-- BeginCacheSizeJS --> 
<%@ Language="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<HTML> 
<HEAD> 
<<<<<<< HEAD
<title>CacheSize Property Example (JScript)</title> 
=======
<title>CacheSize property example (JScript)</title> 
>>>>>>> master
<style> 
<!-- 
body { 
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
</HEAD> 
<BODY> 
<<<<<<< HEAD
<h1>CacheSize Property Example (JScript)</h1> 
=======
<h1>CacheSize property example (JScript)</h1> 
>>>>>>> master
<% 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsCustomer = Server.CreateObject("ADODB.Recordset"); 
 // caching variables 
 var Now = new Date(); 
 var Start = Now.getTime(); 
 var End, Cache, NoCache 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn) 
 
 // open a recordset on the Employee table using client-side cursor 
 rsCustomer.CursorLocation = adUseClient; 
 rsCustomer.Open("Customers", strCnxn); 
 
 // loop through the recordset 20 times 
 for (var i=1; i<=20; i++) 
 { 
 rsCustomer.MoveFirst(); 
 while (!rsCustomer.EOF) 
 { 
 // do something with the record 
 var strTemp = new String(rsCustomer("CompanyName")); 
 rsCustomer.MoveNext(); 
 } 
 } 
 
 Now = new Date(); 
 End = Now.getTime(); 
 NoCache = End - Start; 
 
 // cache records in groups of 30 
 rsCustomer.MoveFirst(); 
 rsCustomer.CacheSize = 30; 
 
 Now = new Date(); 
 Start = Now.getTime(); 
 
 // loop through the recordset 20 times 
 for (var i=1; i<=20; i++) 
 { 
 rsCustomer.MoveFirst(); 
 while (!rsCustomer.EOF) 
 { 
 // do something with the record 
 var strTemp = new String(rsCustomer("CompanyName")); 
 rsCustomer.MoveNext(); 
 } 
 } 
 
 Now = new Date(); 
 End = Now.getTime(); 
 var Cache = End - Start; 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsCustomer.State == adStateOpen) 
 rsCustomer.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsCustomer = null; 
 Cnxn = null; 
 } 
%> 
 
 <table border="2"> 
 <tr class="thead2"> 
 <th>No Cache</th> 
 <th>30 Record Cache</th> 
 </tr> 
 <tr class="tbody"> 
 <td><%=NoCache%></td> 
 <td><%=Cache%></td> 
 </tr> 
 </table> 
 
</BODY> 
</HTML> 
<!-- EndCacheSizeJS --> 
 
```

