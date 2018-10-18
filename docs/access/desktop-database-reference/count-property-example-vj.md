---
<span data-ttu-id="1da2a-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade Count (VJ + +): exemplo da propriedade Count (VJ + +) === título: exemplo da propriedade Count (VJ + +) TOCTitle: exemplo da propriedade Count (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="1da2a-101"><<<<<<< HEAD title: Count Property Example (VJ++) TOCTitle: Count Property Example (VJ++) ======= title: Count property example (VJ++) TOCTitle: Count property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="1da2a-102">ms:assetid de mestre: 749de00a-7530-ea04-558c-34277c4d2f61 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249478(v=office.15) ms:contentKeyID: ms.date 48545666: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="1da2a-102">master ms:assetid: 749de00a-7530-ea04-558c-34277c4d2f61 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249478(v=office.15) ms:contentKeyID: 48545666 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="1da2a-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="1da2a-103"><<<<<<< HEAD</span></span>
# <a name="count-property-example-vj"></a><span data-ttu-id="1da2a-104">Exemplo da propriedade Count (VJ++)</span><span class="sxs-lookup"><span data-stu-id="1da2a-104">Count Property Example (VJ++)</span></span>
=======
# <a name="count-property-example-vj"></a><span data-ttu-id="1da2a-105">Exemplo da propriedade Count (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="1da2a-105">Count property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="1da2a-106">mestre</span><span class="sxs-lookup"><span data-stu-id="1da2a-106">master</span></span>


<span data-ttu-id="1da2a-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1da2a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1da2a-108">Este exemplo demonstra a propriedade [Count](count-property-ado.md) com duas coleções do banco de dados de ***funcionários*** .</span><span class="sxs-lookup"><span data-stu-id="1da2a-108">This example demonstrates the [Count](count-property-ado.md) property with two collections in the ***Employees*** database.</span></span> <span data-ttu-id="1da2a-109">A propriedade obtém a quantidade de objetos em cada coleção e define o limite máximo de loops que enumeram essas coleções.</span><span class="sxs-lookup"><span data-stu-id="1da2a-109">The property obtains the number of objects in each collection, and sets the upper limit for loops that enumerate these collections.</span></span> <span data-ttu-id="1da2a-110">Outra maneira para enumerar essas coleções sem usar a propriedade **Count** seria usar instruções.</span><span class="sxs-lookup"><span data-stu-id="1da2a-110">Another way to enumerate these collections without using the **Count** property would be to use statements.</span></span>

```java 
 
// BeginCountJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class CountX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 CountX(); 
 System.exit(0); 
 } 
 
 // CountX function 
 
 static void CountX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 int intLoop; 
 int intDisplaySize = 20; 
 int recCount=0; 
 
 try 
 { 
 rstEmployees = new Recordset(); 
 
 // Open recordset with data from Employees table. 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Print information about Fields collection. 
 System.out.println(rstEmployees.getFields().getCount() + 
 " Fields in Employees"); 
 for ( intLoop = 0; intLoop < 
 rstEmployees.getFields().getCount(); intLoop++) 
 { 
 System.out.println("\t" + 
 rstEmployees.getFields().getItem(intLoop).getName()); 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Print information about Properties collection. 
 System.out.println(rstEmployees.getProperties().getCount() + 
 " Properties in Employees"); 
 for ( intLoop = 0; intLoop < 
 rstEmployees.getProperties().getCount(); intLoop++) 
 { 
 System.out.println("\t" + 
 rstEmployees.getProperties().getItem(intLoop).getName()); 
 recCount++; 
 if ( recCount >= intDisplaySize) 
 { 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 recCount = 0; 
 } 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstEmployees.getActiveConnection()==null) 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 else 
 { 
 // As passing a Recordset, check for null pointer first. 
 if (rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
 } 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
 
// EndCountJ 
```

