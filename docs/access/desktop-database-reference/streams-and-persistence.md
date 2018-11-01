---
title: Objetos Stream e persistência
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 65fda92e28aab278fde4dafba4e94c576827370a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881745"
---
# <a name="streams-and-persistence"></a>Objetos Stream e persistência


**Aplica-se a**: Access 2013, o Office 2013

O método [Save](save-method-ado.md) do objeto [Recordset](recordset-object-ado.md) armazena, ou *mantém*, um **Recordset** em um arquivo, e o método [Open](open-method-ado-recordset.md) restaura **Recordset** desse arquivo.

Com o ADO 2.5, os métodos **Save** e **Open** também podem manter um **Recordset** em um objeto [Stream](stream-object-ado.md). Esse recurso é especialmente útil quando se trabalha com o RDS (Remote Data Service) e o ASP (Active Server Pages).

Para obter mais informações sobre como usar a persistência em páginas ASP, consulte a documentação atual do ASP.

Alguns cenários a seguir mostram como usar os objetos **Stream** e a persistência.

## <a name="scenario-1"></a>Cenário 1

Este cenário simplesmente salva um **Recordset** em um arquivo e, em seguida, em um **Stream**. Em seguida, ele abre o fluxo persistente em outro **Recordset**.

```vb 
 
Dim rs1 As ADODB.Recordset 
Dim rs2 As ADODB.Recordset 
Dim stm As ADODB.Stream 
 
Set rs1 = New ADODB.Recordset 
Set rs2 = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
rs1.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText 
rs1.Save "c:\myfolder\mysubfolder\myrs.xml", adPersistXML 
rs1.Save stm, adPersistXML 
rs2.Open stm 
```

## <a name="scenario-2"></a>Cenário 2

Este cenário mantém um **Recordset** em um **Stream** no formato XML. Em seguida, ele lê **Stream** em uma sequência de caracteres que você pode examinar, manipular ou exibir.

```vb 
 
Dim rs As ADODB.Recordset 
Dim stm As ADODB.Stream 
Dim strRst As String 
 
Set rs = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
' Open, save, and close the recordset. 
rs.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
rs.Save stm, adPersistXML 
rs.Close 
Set rs = nothing 
 
' Put saved Recordset into a string variable. 
strRst = stm.ReadText(adReadAll) 
 
' Examine, manipulate, or display the XML data. 
... 
```

## <a name="scenario-3"></a>Cenário 3

Este código de exemplo mostra um código ASP mantendo um **Recordset** como XML diretamente no objeto **Response**:

```vb 
 
... 
<% 
response.ContentType = "text/xml" 
 
' Create and open a Recordset. 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select * from Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
 
' Save Recordset directly into output stream. 
rs.Save Response, adPersistXML 
 
' Close Recordset. 
rs.Close 
Set rs = nothing 
%> 
... 
```

## <a name="scenario-4"></a>Cenário 4

Neste cenário, o código ASP cria o conteúdo de **Recordset** em formato ADTG para o cliente. O [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) pode usar esses dados para criar um **Recordset** desconectado.

Uma nova propriedade [URL](datacontrol-object-rds.md) no [DataControl](url-property-rds.md) do RDS aponta para a página .asp que gera o **Recordset**. Isso significa que um objeto **Recordset** pode ser obtido sem que o RDS utilize o objeto [DataFactory](datafactory-object-rdsserver.md) de servidor ou o usuário precise criar um objeto corporativo, o que simplifica bastante o modelo de programação RDS.

Código de servidor, denominado https://server/directory/recordset.asp:

```vb 
 
<% 
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select au_fname, au_lname, phone from Authors", ""& _ 
 "Provider=sqloledb;Data Source=MyServer;" & _ 
 "Initial Catalog=Pubs;Integrated Security=SSPI;" 
response.ContentType = "multipart/mixed" 
rs.Save response, adPersistADTG 
%> 
```

Código de cliente:

```html 
 
<HTML> 
<HEAD> 
<TITLE>RDS Query Page</TITLE> 
</HEAD> 
<body> 
<CENTER> 
<H1>Remote Data Service 2.5</H1> 
<TABLE DATASRC="#DC1"> 
 <TR> 
 <TD><SPAN DATAFLD="au_fname"></SPAN></TD> 
 <TD><SPAN DATAFLD="au_lname"></SPAN></TD> 
 <TD><SPAN DATAFLD="phone"></SPAN></TD> 
 </TR> 
</TABLE> 

<BR> 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
 ID=DC1 HEIGHT=1 WIDTH = 1> 
 <PARAM NAME="URL" VALUE="https://server/directory/recordset.asp"> 
</OBJECT> 
 
</SCRIPT> 
</BODY> 
</HTML> 
```

Os desenvolvedores também podem optar por usar um objeto **Recordset** no cliente:

```vb
... 
function GetRs() 
 { 
 rs = CreateObject("ADODB.Recordset"); 
 rs.Open "https://server/directory/recordset.asp" 
 DC1.SourceRecordset = rs; 
 } 
... 
```

