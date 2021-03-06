---
title: Exemplo das propriedades NumericScale e Precision (VC++)
TOCTitle: NumericScale and Precision properties example (VC++)
ms:assetid: da4bec90-b039-1764-3b8b-c74bb725da61
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250098(v=office.15)
ms:contentKeyID: 48548078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d452408337ed1aabfb94a224af4c1f1ee84a3961
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288536"
---
# <a name="numericscale-and-precision-properties-example-vc"></a>Exemplo das propriedades NumericScale e Precision (VC++)


**Aplica-se ao:** Access 2013, Office 2013

Este exemplo demonstra as propriedades [NumericScale](numericscale-property-adox.md) e [Precision](precision-property-adox.md) do objeto [Column](column-object-adox.md). Este código exibe o valor delas para a tabela **Order Details** do banco de dados *Northwind*.

```cpp 
 
// BeginNumericScalePrecCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void NumericScalePrecX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 NumericScalePrecX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// NumericScalePrecX Function // 
// // 
////////////////////////////////////////////////////////// 
void NumericScalePrecX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 _ColumnPtr m_pColumn = NULL; 
 
 //Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 //Declare string variables 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 
 // Connect the catalog. 
 m_pCnn->Open (strCnn, "", "", NULL); 
 
 m_pCatalog->PutActiveConnection(variant_t((IDispatch *)m_pCnn)); 
 
 // Retrieve the Order Details table 
 m_pTable = m_pCatalog->Tables->GetItem("Order Details"); 
 
 // Display numeric scale and precision of 
 // small integer fields. 
 _variant_t vIndex; 
 for (long lIndex=0; lIndex < m_pTable->Columns->Count; lIndex++) 
 { 
 vIndex = lIndex ; 
 m_pColumn = m_pTable->Columns->GetItem(vIndex); 
 if(m_pColumn->Type == adSmallInt) 
 { 
 cout << "Column: " << m_pColumn->GetName() << endl; 
 cout << "Numeric scale: " << (_bstr_t) m_pColumn-> 
 GetNumericScale() << endl; 
 cout << "Precision: " << m_pColumn->GetPrecision() << 
 endl; 
 } 
 } 
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
 cout << "Error occured in NumericScalePrecX...."<< endl; 
 } 
} 
// EndNumericScalePrecCpp 
```

