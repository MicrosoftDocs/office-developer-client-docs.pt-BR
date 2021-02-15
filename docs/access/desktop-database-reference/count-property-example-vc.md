---
title: Exemplo da propriedade Count (VC++)
TOCTitle: Count property example (VC++)
ms:assetid: 5e3d817b-05bf-c96e-67ba-c41f06c367af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249340(v=office.15)
ms:contentKeyID: 48545134
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f21bb3c2f20f0d9d446a099fd6322928e626616
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295447"
---
# <a name="count-property-example-vc"></a><span data-ttu-id="a9704-102">Exemplo da propriedade Count (VC++)</span><span class="sxs-lookup"><span data-stu-id="a9704-102">Count property example (VC++)</span></span>


<span data-ttu-id="a9704-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9704-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9704-104">Este exemplo demonstra a propriedade [Count](count-property-ado.md) com duas coleções no banco de dados ***Employee***.</span><span class="sxs-lookup"><span data-stu-id="a9704-104">This example demonstrates the [Count](count-property-ado.md) property with two collections in the ***Employee*** database.</span></span> <span data-ttu-id="a9704-105">A propriedade obtém a quantidade de objetos em cada coleção e define o limite máximo de loops que enumeram essas coleções.</span><span class="sxs-lookup"><span data-stu-id="a9704-105">The property obtains the number of objects in each collection, and sets the upper limit for loops that enumerate these collections.</span></span> <span data-ttu-id="a9704-106">Outra maneira de enumerar essas coleções sem usar a **propriedade Count** seria usar instruções.</span><span class="sxs-lookup"><span data-stu-id="a9704-106">Another way to enumerate these collections without using the **Count** property would be to use statements.</span></span>

```cpp 
 
// BeginCountCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include<conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void CountX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
/////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 CountX(); 
 
 //Wait here for user to see the output.. 
 printf("\nPress any key to Exit..."); 
 getch(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// CountX Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void CountX() 
{ 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace 
 _RecordsetPtr pRstEmployee = NULL; 
 
 //Define Other Variables 
 HRESULT hr = S_OK; 
 _variant_t Index; 
 Index.vt = VT_I2; 
 int j = 0; 
 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 // Open recordset with data from Employee table. 
 TESTHR(pRstEmployee.CreateInstance(__uuidof(Recordset))); 
 pRstEmployee->Open("Employee", strCnn, adOpenForwardOnly, 
 adLockReadOnly, adCmdTable); 
 
 // Print information about Fields collection. 
 printf("%d Fields in Employee\n", pRstEmployee->Fields->Count); 
 for (int intLoop = 0; 
 intLoop <= (pRstEmployee->Fields->Count-1); 
 intLoop++) 
 { 
 Index.iVal = intLoop; 
 printf(" %s\n",(LPSTR) pRstEmployee->Fields-> 
 GetItem(Index)->Name); 
 } 
 
 // Print information about Properties collection. 
 printf("\n%d Properties in Employee\n", pRstEmployee-> 
 Properties->Count); 
 for (intLoop = 0; 
 intLoop <= (pRstEmployee->Properties->Count - 1); 
 intLoop++) 
 { 
 j++; 
 Index.iVal = intLoop; 
 printf(" %s\n" ,(LPSTR)pRstEmployee->Properties-> 
 GetItem(Index)->Name); 
 if (((j % 23) == 0) || (intLoop == 11)) 
 { 
 printf("\nPress any key to continue..."); 
 getch(); 
 
 //Clear the screen for the next display 
 system("cls"); 
 j = 0; 
 } 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify user of any errors that result from 
 // executing the query. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstEmployee->GetActiveConnection(); 
 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
 break; 
 case VT_DISPATCH: 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 // Clean up objects before exit. 
 if (pRstEmployee) 
 if (pRstEmployee->State == adStateOpen) 
 pRstEmployee->Close(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0; i < nCount; i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("Error number: %x\t%s\n",pErr->Number, 
 pErr->Description); 
 } 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void PrintComError(_com_error &e) 
{ 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print Com errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
// EndCountCpp 
```

