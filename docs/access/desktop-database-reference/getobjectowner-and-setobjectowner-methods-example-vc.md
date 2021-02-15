---
title: Exemplo dos métodos GetObjectOwner e SetObjectOwner (VC++)
TOCTitle: GetObjectOwner and SetObjectOwner methods example (VC++)
ms:assetid: af38cc5c-4475-20fa-edcd-a439e1ffbf99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249835(v=office.15)
ms:contentKeyID: 48547096
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1227d60555dcb8da919e75bfa773fd64103a956
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292276"
---
# <a name="getobjectowner-and-setobjectowner-methods-example-vc"></a><span data-ttu-id="c197b-102">Exemplo dos métodos GetObjectOwner e SetObjectOwner (VC++)</span><span class="sxs-lookup"><span data-stu-id="c197b-102">GetObjectOwner and SetObjectOwner methods example (VC++)</span></span>


<span data-ttu-id="c197b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c197b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c197b-104">Este exemplo demonstra os métodos [GetObjectOwner](getobjectowner-method-adox.md) e [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox).</span><span class="sxs-lookup"><span data-stu-id="c197b-104">This example demonstrates the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span> <span data-ttu-id="c197b-105">Este código assume a existência do grupo Accounting (consulte o exemplo dos métodos Append e ChangePassword de grupos e usuários [(VC++)](groups-and-users-append-changepassword-methods-example-vc.md) para ver como adicionar esse grupo ao sistema).</span><span class="sxs-lookup"><span data-stu-id="c197b-105">This code assumes the existence of the group Accounting (see the [Groups and Users Append, ChangePassword methods example (VC++)](groups-and-users-append-changepassword-methods-example-vc.md) to see how to add this group to the system).</span></span> <span data-ttu-id="c197b-106">O proprietário da tabela Categories é definido como Accounting.</span><span class="sxs-lookup"><span data-stu-id="c197b-106">The owner of the Categories table is set to Accounting.</span></span>

```cpp 
 
// BeginOwnersCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void OwnersX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 OwnersX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// OwnersX Function // 
// // 
////////////////////////////////////////////////////////// 
void OwnersX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _TablePtr m_pTable = NULL; 
 _CatalogPtr m_pCatalog = NULL; 
 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 TESTHR(hr = m_pTable.CreateInstance(__uuidof(Table))); 
 
 //Open the Catalog. 
 m_pCatalog->PutActiveConnection( 
 "Provider='Microsoft.JET.OLEDB.4.0';" "data source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';" 
 "jet oledb:system database='c:\\Program Files\\Microsoft Office\\" 
 "Office\\system.mdw'"); 
 
 //Print the original owner of Categories 
 _bstr_t strOwner = m_pCatalog->GetObjectOwner("Categories", 
 adPermObjTable); 
 cout << "Owner of Categories: " << strOwner << "\n" << endl; 
 int iLineCnt = 2; 
 
 //Create and append new group with a string. 
 m_pCatalog->Groups->Append("Accounting"); 
 
 //Set the owner of Categories to Accounting. 
 m_pCatalog->SetObjectOwner("Categories", 
 adPermObjTable,"Accounting"); 
 
 _variant_t vIndex; 
 //List the owners of all tables and columns in the catalog. 
 for (long iIndex = 0; iIndex < m_pCatalog->Tables->Count; iIndex++) 
 { 
 vIndex = iIndex; 
 m_pTable = m_pCatalog->Tables->GetItem(vIndex); 
 cout << "Table: " << m_pTable->Name << endl; 
 cout << " Owner: " << m_pCatalog-> 
 GetObjectOwner(m_pTable->Name,adPermObjTable) << endl; 
 if (iLineCnt%16 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 iLineCnt = iLineCnt + 2; 
 } 
 
 //Restore the original owner of Categories 
 m_pCatalog->SetObjectOwner("Categories",adPermObjTable,strOwner); 
 
 //Delete Accounting 
 m_pCatalog->Groups->Delete("Accounting"); 
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
// EndOwnersCpp 
```

