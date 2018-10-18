---
<span data-ttu-id="71dec-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade Status (VJ + +): exemplo da propriedade Status (VJ + +) === título: exemplo da propriedade Status (VJ + +) TOCTitle: exemplo da propriedade Status (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="71dec-101"><<<<<<< HEAD title: Status Property Example (VJ++) TOCTitle: Status Property Example (VJ++) ======= title: Status property example (VJ++) TOCTitle: Status property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="71dec-102">ms:assetid de mestre: bdfc1b26-b384-e7e5-ff4b-d63ed62f70ca ms:mtpsurl: https://msdn.microsoft.com/library/JJ249922(v=office.15) ms:contentKeyID: ms.date 48547452: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="71dec-102">master ms:assetid: bdfc1b26-b384-e7e5-ff4b-d63ed62f70ca ms:mtpsurl: https://msdn.microsoft.com/library/JJ249922(v=office.15) ms:contentKeyID: 48547452 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="71dec-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="71dec-103"><<<<<<< HEAD</span></span>
# <a name="status-property-example-vj"></a><span data-ttu-id="71dec-104">Exemplo da propriedade Status (VJ++)</span><span class="sxs-lookup"><span data-stu-id="71dec-104">Status Property Example (VJ++)</span></span>
=======
# <a name="status-property-example-vj"></a><span data-ttu-id="71dec-105">Exemplo da propriedade status (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="71dec-105">Status property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="71dec-106">mestre</span><span class="sxs-lookup"><span data-stu-id="71dec-106">master</span></span>


<span data-ttu-id="71dec-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="71dec-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="71dec-108">Este exemplo utiliza a propriedade [Status](status-property-ado-recordset.md) para exibir quais registros foram modificados em uma operação em lote antes da ocorrência de uma atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="71dec-108">This example uses the [Status](status-property-ado-recordset.md) property to display which records have been modified in a batch operation before a batch update has occurred.</span></span>

```java 
 
// BeginStatusJ 
import java.io.*; 
import com.ms.wfc.data.*; 
 
public class StatusX 
{ 
 // The main entry point of the application. 
 
 public static void main (String[] args) 
 { 
 StatusX(); 
 System.exit(0); 
 } 
 // StatusX Function 
 
 static void StatusX() 
 { 
 // Define ADO Objects. 
 Recordset rstTitles = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 
 try 
 { 
 // Open Recordset for batch update. 
 rstTitles = new Recordset(); 
 rstTitles.setCursorType(AdoEnums.CursorType.KEYSET); 
 rstTitles.setLockType(AdoEnums.LockType.BATCHOPTIMISTIC); 
 rstTitles.open("Titles", strCnn, AdoEnums.CursorType.KEYSET, 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.TABLE); 
 
 // Change the type of psychology titles. 
 while(!rstTitles.getEOF()) 
 { 
 if(rstTitles.getField("Type").getString().trim(). 
 equals(new String("psychology"))) 
 rstTitles.getField("Type").setString("self_help"); 
 
 rstTitles.moveNext(); 
 } 
 
 // Display Title ID and status. 
 rstTitles.moveFirst(); 
 
 while(!rstTitles.getEOF()) 
 { 
 if(rstTitles.getStatus()==AdoEnums.RecordStatus.MODIFIED) 
 System.out.println(rstTitles.getField("title_id"). 
 getString() + "- Modified"); 
 else 
 System.out.println(rstTitles.getField("title_id"). 
 getString()); 
 rstTitles.moveNext(); 
 } 
 
 // Cancel the update because this is a demonstration. 
 rstTitles.cancelBatch(); 
 
 System.out.println("Press <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a Recordset, check for the null pointer first. 
 if(rstTitles != null) 
 { 
 PrintProviderError(rstTitles.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 // System read requires this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstTitles != null) 
 if (rstTitles.getState() == 1) 
 rstTitles.close(); 
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
// EndStatusJ 
```

