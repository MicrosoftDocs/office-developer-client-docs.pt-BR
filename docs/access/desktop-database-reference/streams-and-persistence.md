---
title: Objetos Stream e persistência
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a90031ac2f6d573631063edb0faf4893c2320d03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944379"
---
# <a name="streams-and-persistence"></a><span data-ttu-id="5346e-102">Objetos Stream e persistência</span><span class="sxs-lookup"><span data-stu-id="5346e-102">Streams and persistence</span></span>


<span data-ttu-id="5346e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5346e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5346e-104">O método [Save](save-method-ado.md) do objeto [Recordset](recordset-object-ado.md) armazena, ou *mantém*, um **Recordset** em um arquivo, e o método [Open](open-method-ado-recordset.md) restaura **Recordset** desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="5346e-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="5346e-p101">Com o ADO 2.5, os métodos **Save** e **Open** também podem manter um **Recordset** em um objeto [Stream](stream-object-ado.md). Esse recurso é especialmente útil quando se trabalha com o RDS (Remote Data Service) e o ASP (Active Server Pages).</span><span class="sxs-lookup"><span data-stu-id="5346e-p101">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well. This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="5346e-107">Para obter mais informações sobre como usar a persistência em páginas ASP, consulte a documentação atual do ASP.</span><span class="sxs-lookup"><span data-stu-id="5346e-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="5346e-108">Alguns cenários a seguir mostram como usar os objetos **Stream** e a persistência.</span><span class="sxs-lookup"><span data-stu-id="5346e-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="5346e-109">Cenário 1</span><span class="sxs-lookup"><span data-stu-id="5346e-109">Scenario 1</span></span>

<span data-ttu-id="5346e-p102">Este cenário simplesmente salva um **Recordset** em um arquivo e, em seguida, em um **Stream**. Em seguida, ele abre o fluxo persistente em outro **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5346e-p102">This scenario simply saves a **Recordset** to a file and then to a **Stream**. It then opens the persisted stream into another **Recordset**.</span></span>

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

## <a name="scenario-2"></a><span data-ttu-id="5346e-112">Cenário 2</span><span class="sxs-lookup"><span data-stu-id="5346e-112">Scenario 2</span></span>

<span data-ttu-id="5346e-p103">Este cenário mantém um **Recordset** em um **Stream** no formato XML. Em seguida, ele lê **Stream** em uma sequência de caracteres que você pode examinar, manipular ou exibir.</span><span class="sxs-lookup"><span data-stu-id="5346e-p103">This scenario persists a **Recordset** into a **Stream** in XML format. It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

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

## <a name="scenario-3"></a><span data-ttu-id="5346e-115">Cenário 3</span><span class="sxs-lookup"><span data-stu-id="5346e-115">Scenario 3</span></span>

<span data-ttu-id="5346e-116">Este código de exemplo mostra um código ASP mantendo um **Recordset** como XML diretamente no objeto **Response**:</span><span class="sxs-lookup"><span data-stu-id="5346e-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

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

## <a name="scenario-4"></a><span data-ttu-id="5346e-117">Cenário 4</span><span class="sxs-lookup"><span data-stu-id="5346e-117">Scenario 4</span></span>

<span data-ttu-id="5346e-p104">Neste cenário, o código ASP cria o conteúdo de **Recordset** em formato ADTG para o cliente. O [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) pode usar esses dados para criar um **Recordset** desconectado.</span><span class="sxs-lookup"><span data-stu-id="5346e-p104">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client. The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="5346e-p105">Uma nova propriedade [URL](datacontrol-object-rds.md) no [DataControl](url-property-rds.md) do RDS aponta para a página .asp que gera o **Recordset**. Isso significa que um objeto **Recordset** pode ser obtido sem que o RDS utilize o objeto [DataFactory](datafactory-object-rdsserver.md) de servidor ou o usuário precise criar um objeto corporativo, o que simplifica bastante o modelo de programação RDS.</span><span class="sxs-lookup"><span data-stu-id="5346e-p105">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**. This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object. This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="5346e-123">Código de servidor, denominado https://server/directory/recordset.asp:</span><span class="sxs-lookup"><span data-stu-id="5346e-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

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

<span data-ttu-id="5346e-124">Código de cliente:</span><span class="sxs-lookup"><span data-stu-id="5346e-124">Client-side code:</span></span>

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

<span data-ttu-id="5346e-125">Os desenvolvedores também podem optar por usar um objeto **Recordset** no cliente:</span><span class="sxs-lookup"><span data-stu-id="5346e-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

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

