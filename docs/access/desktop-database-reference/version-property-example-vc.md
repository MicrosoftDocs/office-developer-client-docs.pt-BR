---
title: Exemplo da propriedade Version (VC++)
TOCTitle: Version Property Example (VC++)
ms:assetid: deda3998-52cd-0068-7f8c-e58c71802226
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250130(v=office.15)
ms:contentKeyID: 48548201
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6723d43965975f8ad83f60937e7226cd269b688d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465017"
---
# <a name="version-property-example-vc"></a><span data-ttu-id="adef7-102">Exemplo da propriedade Version (VC++)</span><span class="sxs-lookup"><span data-stu-id="adef7-102">Version Property Example (VC++)</span></span>


<span data-ttu-id="adef7-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="adef7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="adef7-p101">Este exemplo utiliza a propriedade [Version](version-property-ado.md) de um objeto [Connection](connection-object-ado.md) para exibir a versão atual do ADO. Ele também utiliza várias propriedades dinâmicas para mostrar:</span><span class="sxs-lookup"><span data-stu-id="adef7-p101">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version. It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="adef7-106">o nome e a versão do DBMS atual.</span><span class="sxs-lookup"><span data-stu-id="adef7-106">the current DBMS name and version.</span></span>

  - <span data-ttu-id="adef7-107">a versão do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="adef7-107">OLE DB version.</span></span>

  - <span data-ttu-id="adef7-108">o nome e a versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="adef7-108">provider name and version.</span></span>

  - <span data-ttu-id="adef7-109">a versão do ODBC.</span><span class="sxs-lookup"><span data-stu-id="adef7-109">ODBC version.</span></span>

  - <span data-ttu-id="adef7-110">o nome e a versão do driver do ODBC.</span><span class="sxs-lookup"><span data-stu-id="adef7-110">ODBC driver name and version.</span></span>

<!-- end list -->

```cpp 
 
// BeginVersionCpp 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void VersionX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 VersionX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// VersionX Function // 
// // 
////////////////////////////////////////////////////////// 
void VersionX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strCnn("driver={SQL Server};server='MySqlServer';" 
 "user id='MyUserId';password='MyPassword';database='pubs';"); 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 
 try 
 { 
 // Open connection. 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 
 printf("ADO Version : %s\n\n",(LPCSTR) pConnection->Version); 
 printf("DBMS Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("DBMS Name")->Value); 
 printf("DBMS Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("DBMS Version")->Value); 
 printf("OLE DB Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("OLE DB Version")->Value); 
 printf("Provider Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Provider Name")->Value); 
 printf("Provider Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Provider Version")->Value); 
 printf("Driver Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver Name")->Value); 
 printf("Driver Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver Version")->Value); 
 printf("Driver ODBC Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver ODBC Version")->Value); 
 
 } 
 
 catch (_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
////////////////////////////////////////////////////////// 
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
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
 } 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
////////////////////////////////////////////////////////// 
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
// EndVersionCpp 
```

