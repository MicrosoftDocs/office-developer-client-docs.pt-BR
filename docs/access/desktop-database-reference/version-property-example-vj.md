---
<span data-ttu-id="8e88e-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade Version (VJ + +): exemplo da propriedade Version (VJ + +) === título: exemplo da propriedade Version (VJ + +) TOCTitle: exemplo da propriedade Version (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="8e88e-101"><<<<<<< HEAD title: Version Property Example (VJ++) TOCTitle: Version Property Example (VJ++) ======= title: Version property example (VJ++) TOCTitle: Version property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="8e88e-102">ms:assetid de mestre: c4f007b8-177d-967e-7f3b-a8945264099b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249963(v=office.15) ms:contentKeyID: ms.date 48547600: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="8e88e-102">master ms:assetid: c4f007b8-177d-967e-7f3b-a8945264099b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249963(v=office.15) ms:contentKeyID: 48547600 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8e88e-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="8e88e-103"><<<<<<< HEAD</span></span>
# <a name="version-property-example-vj"></a><span data-ttu-id="8e88e-104">Exemplo da propriedade Version (VJ++)</span><span class="sxs-lookup"><span data-stu-id="8e88e-104">Version Property Example (VJ++)</span></span>
=======
# <a name="version-property-example-vj"></a><span data-ttu-id="8e88e-105">Exemplo da propriedade Version (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="8e88e-105">Version property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="8e88e-106">mestre</span><span class="sxs-lookup"><span data-stu-id="8e88e-106">master</span></span>


<span data-ttu-id="8e88e-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e88e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e88e-p101">Este exemplo utiliza a propriedade [Version](version-property-ado.md) de um objeto [Connection](connection-object-ado.md) para exibir a versão atual do ADO. Ele também utiliza várias propriedades dinâmicas para mostrar:</span><span class="sxs-lookup"><span data-stu-id="8e88e-p101">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version. It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="8e88e-110">o nome e a versão do DBMS atual.</span><span class="sxs-lookup"><span data-stu-id="8e88e-110">the current DBMS name and version.</span></span>

  - <span data-ttu-id="8e88e-111">a versão do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8e88e-111">OLE DB version.</span></span>

  - <span data-ttu-id="8e88e-112">o nome e a versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="8e88e-112">provider name and version.</span></span>

  - <span data-ttu-id="8e88e-113">a versão do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8e88e-113">ODBC version.</span></span>

  - <span data-ttu-id="8e88e-114">o nome e a versão do driver do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8e88e-114">ODBC driver name and version.</span></span>

<!-- end list -->

```java 
 
// BeginVersionJ 
import com.ms.wfc.data.*; 
import java.io.*; 
 
public class VersionX 
{ 
 // The main entry point of the application. 
 public static void main (String[] args) 
 { 
 VersionX(); 
 System.exit(0); 
 } 
 // VersionX Function 
 static void VersionX() 
 { 
 // Define ADO Objects. 
 Connection cnn1 = null; 
 
 // Declarations. 
 String strCnn = "Driver={SQL Server};Server='MySqlServer';" + 
 "User ID='MyUserID';Password='MyPassword';database='Pubs';"; 
 String strVersionInfo; 
 BufferedReader in = new 
 BufferedReader(new InputStreamReader(System.in)); 
 try 
 { 
 // Open connection. 
 cnn1 = new Connection(); 
 cnn1.open(strCnn); 
 
 strVersionInfo = "\tADO Version:\t\t" + 
 cnn1.getVersion().toString()+"\n"+ 
 "\tDBMS Name:\t\t" + 
 cnn1.getProperties().getItem("DBMS Name").getString() +"\n"+ 
 "\tDBMS Version:\t\t"+ 
 cnn1.getProperties().getItem("DBMS Version").getString() + 
 "\n" + "\tOLE DB Version:\t\t" + 
 cnn1.getProperties().getItem("OLE DB Version").getString()+ 
 "\n" + "\tProvider Name:\t\t" + 
 cnn1.getProperties().getItem("Provider Name").getString() + 
 "\n" + "\tProvider Version:\t" + 
 cnn1.getProperties().getItem("Provider Version"). 
 getString() + "\n" + "\tDriver Name:\t\t" + 
 cnn1.getProperties().getItem("Driver Name").getString() + 
 "\n" + "\tDriver Version:\t\t" + 
 cnn1.getProperties().getItem("Driver Version").getString()+ 
 "\n" + "\tDriver ODBC Version:\t" + 
 cnn1.getProperties().getItem( 
 "Driver ODBC Version").getString()+ "\n"; 
 System.out.println("\n\n" + strVersionInfo); 
 
 System.out.println("Press <Enter> to continue.."); 
 in.readLine(); 
 } 
 // System read requires this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a recordset, check for null pointer first. 
 if(cnn1!= null) 
 { 
 PrintProviderError(cnn1); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 finally 
 { 
 // Cleanup objects before exit. 
 if (cnn1 != null) 
 if (cnn1.getState() == 1) 
 cnn1.close(); 
 } 
 
 } 
 // PrintProviderError Function 
 static void PrintProviderError(Connection cnn1) 
 { 
 // Print Provider Errors from Connection Object. 
 // ErrItem is an item object in the Connections Errors Collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if ( nCount > 0) 
 { 
 // Collection ranges from 0 to nCount-1. 
 for ( i=0;i<nCount; i++) 
 { 
 ErrItem = cnn1.getErrors().getItem(i); 
 System.out.println("\t Error Number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription()); 
 } 
 } 
 } 
 // PrintIOError Function 
 static void PrintIOError(java.io.IOException je) 
 { 
 System.out.println("Error: \n"); 
 System.out.println("\t Source: " + je.getClass() + "\n"); 
 System.out.println("\t Description: "+ je.getMessage() + "\n"); 
 } 
} 
// EndVersionJ 
```

