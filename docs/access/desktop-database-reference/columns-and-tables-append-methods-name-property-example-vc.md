---
<<<<<<< Título cabeça: colunas e os métodos Append tabelas, exemplo da propriedade Name (VC + +) TOCTitle: colunas e os métodos Append tabelas, exemplo da propriedade Name (VC + +) === título: colunas e os métodos Append tabelas, exemplo da propriedade Name (VC + +) TOCTitle: Colunas e os métodos Append tabelas, exemplo da propriedade Name (VC + +)
>>>>>>> ms:assetid de mestre: 6586aaed-2556-1d33-c1ab-135a598f7d13 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249392(v=office.15) ms:contentKeyID: ms.date 48545322: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="columns-and-tables-append-methods-name-property-example-vc"></a>Métodos Append de colunas e tabelas, exemplo da propriedade Name (VC++)
=======
# <a name="columns-and-tables-append-methods-name-property-example-vc"></a>Colunas e os métodos Append tabelas, exemplo da propriedade Name (VC + +)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

O código a seguir demonstra como criar uma nova tabela.

```cpp 
 
// BeginCreateTableCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void CreateTableX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 CreateTableX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// CreateTableX Function // 
// // 
////////////////////////////////////////////////////////// 
void CreateTableX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 //Open the catalog 
 m_pCatalog->PutActiveConnection( 
 "Provider='Microsoft.JET.OLEDB.4.0';" "data source='c:\\Program Files\\Microsoft Office" 
 "\\Office\\Samples\\Northwind.mdb';"); 
 
 TESTHR(hr = m_pTable.CreateInstance(__uuidof(Table))); 
 m_pTable->PutName("MyTable"); 
 m_pTable->Columns->Append("Column1",adInteger,0); 
 m_pTable->Columns->Append("Column2",adInteger,0); 
 m_pTable->Columns->Append("Column3",adVarWChar,50); 
 m_pCatalog->Tables->Append( 
 _variant_t((IDispatch *)m_pTable)); 
 printf("Table 'MyTable' is added.\n"); 
 
 // Delete the table as this is a demonstration. 
 m_pCatalog->Tables->Delete("MyTable"); 
 printf("Table 'MyTable' is deleted.\n"); 
 } 
 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 
 catch(...) 
 { 
 cout << "Error occured in include files...."<< endl; 
 } 
} 
// EndCreateTableCpp 
```

