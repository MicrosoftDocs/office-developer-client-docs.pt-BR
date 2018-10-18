---
<span data-ttu-id="75da7-101"><<<<<<< Título cabeça: NumericScale e Precision exemplo das propriedades (VJ + +) TOCTitle: NumericScale e Precision exemplo das propriedades (VJ + +) === título: exemplo das propriedades NumericScale e Precision (VJ + +) TOCTitle: NumericScale e Exemplo das propriedades Precision (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="75da7-101"><<<<<<< HEAD title: NumericScale and Precision Properties Example (VJ++) TOCTitle: NumericScale and Precision Properties Example (VJ++) ======= title: NumericScale and Precision properties example (VJ++) TOCTitle: NumericScale and Precision properties example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="75da7-102">ms:assetid de mestre: 9b6fc40c-b740-ede0-d69d-546eb5d40c95 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249707(v=office.15) ms:contentKeyID: ms.date 48546574: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="75da7-102">master ms:assetid: 9b6fc40c-b740-ede0-d69d-546eb5d40c95 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249707(v=office.15) ms:contentKeyID: 48546574 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="75da7-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="75da7-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-and-precision-properties-example-vj"></a><span data-ttu-id="75da7-104">Exemplo das propriedades NumericScale e Precision (VJ++)</span><span class="sxs-lookup"><span data-stu-id="75da7-104">NumericScale and Precision Properties Example (VJ++)</span></span>
=======
# <a name="numericscale-and-precision-properties-example-vj"></a><span data-ttu-id="75da7-105">Exemplo das propriedades NumericScale e Precision (VJ + +)</span><span class="sxs-lookup"><span data-stu-id="75da7-105">NumericScale and Precision properties example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="75da7-106">mestre</span><span class="sxs-lookup"><span data-stu-id="75da7-106">master</span></span>


<span data-ttu-id="75da7-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75da7-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75da7-108">Este exemplo usa as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md) para exibir a escala numérica e a precisão de campos na tabela ***Discounts*** do banco de dados ***Pubs***.</span><span class="sxs-lookup"><span data-stu-id="75da7-108">This example uses the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties to display the numeric scale and precision of fields in the ***Discounts*** table of the ***Pubs*** database.</span></span>

```java 
 
// BeginNumericScaleJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class NumericScaleX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 NumericScaleX(); 
 System.exit(0); 
 } 
 
 // NumericScaleX function 
 
 static void NumericScaleX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstDiscounts = null; 
 Field fldTemp = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 int intLoop; 
 
 try 
 { 
 rstDiscounts = new Recordset(); 
 
 // Open recordset. 
 rstDiscounts.open("Discounts", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Display numeric scale and precision of 
 // numeric and small integer fields. 
 for ( intLoop=0; intLoop < 
 rstDiscounts.getFields().getCount();intLoop++) 
 { 
 fldTemp = rstDiscounts.getFields().getItem(intLoop); 
 if((fldTemp.getType()== AdoEnums.DataType.NUMERIC) | 
 (fldTemp.getType()== AdoEnums.DataType.SMALLINT)) 
 { 
 System.out.println("\nField: " 
 + fldTemp.getName()); 
 System.out.println("\nNumeric scale: " 
 + fldTemp.getNumericScale()); 
 System.out.println("\nPrecision: " 
 + fldTemp.getPrecision()); 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 } 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstDiscounts != null) 
 { 
 PrintProviderError(rstDiscounts.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
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
 if (rstDiscounts != null) 
 if (rstDiscounts.getState() == 1) 
 rstDiscounts.close(); 
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
// EndNumericScaleJ 
```

