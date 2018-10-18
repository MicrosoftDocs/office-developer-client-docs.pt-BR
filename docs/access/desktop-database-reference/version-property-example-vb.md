---
<span data-ttu-id="96025-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade de versão (VB): exemplo de propriedade de versão (VB) === título: exemplo da propriedade Version (VB) TOCTitle: exemplo da propriedade Version (VB)</span><span class="sxs-lookup"><span data-stu-id="96025-101"><<<<<<< HEAD title: Version Property Example (VB) TOCTitle: Version Property Example (VB) ======= title: Version property example (VB) TOCTitle: Version property example (VB)</span></span>
>>>>>>> <span data-ttu-id="96025-102">ms:assetid de mestre: ffb7b04a-55b9-fa2f-41ec-44af225bd15f ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15) ms:contentKeyID: ms.date 48548968: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="96025-102">master ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15) ms:contentKeyID: 48548968 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="96025-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="96025-103"><<<<<<< HEAD</span></span>
# <a name="version-property-example-vb"></a><span data-ttu-id="96025-104">Exemplo da propriedade Version (VB)</span><span class="sxs-lookup"><span data-stu-id="96025-104">Version Property Example (VB)</span></span>
=======
# <a name="version-property-example-vb"></a><span data-ttu-id="96025-105">Exemplo da propriedade Version (VB)</span><span class="sxs-lookup"><span data-stu-id="96025-105">Version property example (VB)</span></span>
>>>>>>> <span data-ttu-id="96025-106">mestre</span><span class="sxs-lookup"><span data-stu-id="96025-106">master</span></span>


<span data-ttu-id="96025-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="96025-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="96025-p101">Este exemplo utiliza a propriedade [Version](version-property-ado.md) de um objeto [Connection](connection-object-ado.md) para exibir a versão atual do ADO. Ele também utiliza várias propriedades dinâmicas para mostrar:</span><span class="sxs-lookup"><span data-stu-id="96025-p101">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version. It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="96025-110">o nome e a versão do DBMS atual.</span><span class="sxs-lookup"><span data-stu-id="96025-110">the current DBMS name and version.</span></span>

  - <span data-ttu-id="96025-111">a versão do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="96025-111">OLE DB version.</span></span>

  - <span data-ttu-id="96025-112">o nome e a versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="96025-112">provider name and version.</span></span>

  - <span data-ttu-id="96025-113">a versão do ODBC.</span><span class="sxs-lookup"><span data-stu-id="96025-113">ODBC version.</span></span>

  - <span data-ttu-id="96025-114">o nome e a versão do driver do ODBC.</span><span class="sxs-lookup"><span data-stu-id="96025-114">ODBC driver name and version.</span></span>

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

