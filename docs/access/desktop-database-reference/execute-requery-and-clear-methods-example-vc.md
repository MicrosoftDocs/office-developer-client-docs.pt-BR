---
title: Exemplo dos Métodos Execute, Requery e Clear (VC++)
TOCTitle: Execute, Requery, and Clear Methods Example (VC++)
ms:assetid: ac65f1d8-e185-c00a-9ad6-8b6a22529238
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249803(v=office.15)
ms:contentKeyID: 48547008
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d2a973ac975b1835273ac098959097175d50a1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463196"
---
# <a name="execute-requery-and-clear-methods-example-vc"></a>Exemplo dos Métodos Execute, Requery e Clear (VC++)


**Aplica-se a**: Access 2013 | Office 2013

Este exemplo demonstra o método **Execute** ao ser executado a partir de um objeto [Command](command-object-ado.md) e de um objeto [Connection](connection-object-ado.md). Ele também utiliza o método [Requery](requery-method-ado.md) para recuperar dados atuais em um [recordset](recordset-object-ado.md) e o método [Clear](clear-method-ado.md) para limpar o conteúdo da coleção [Errors](errors-collection-ado.md). As funções ExecuteCommand e PrintOutput são necessárias para a execução desse exemplo.

```cpp 
 
// BeginExecuteCpp 
#include <ole2.h> 
#include <stdio.h> 
 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ExecuteX(void); 
void ExecuteCommand(_CommandPtr pCmdTemp, _RecordsetPtr pRstTemp); 
void PrintOutput(_RecordsetPtr pRstTemp); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
//////////////////////////////// 
// Main Function // 
//////////////////////////////// 
 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ExecuteX(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////// 
// ExecuteX Function // 
/////////////////////////////////// 
 
void ExecuteX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strSQLChange("UPDATE Titles SET Type = " 
 "'self_help' WHERE Type = 'psychology'"); 
 _bstr_t strSQLRestore("UPDATE Titles SET Type = " 
 "'psychology' WHERE Type = 'self_help'"); 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 _CommandPtr pCmdChange = NULL; 
 _RecordsetPtr pRstTitles = NULL; 
 
 try 
 { 
 // Open connection. 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 
 // Create command object. 
 TESTHR(pCmdChange.CreateInstance(__uuidof(Command))); 
 pCmdChange->ActiveConnection = pConnection; 
 pCmdChange->CommandText = strSQLChange; 
 
 // Open titles table, casting Connection pointer to an 
 // IDispatch type so converted to correct type of variant. 
 TESTHR(pRstTitles.CreateInstance(__uuidof(Recordset))); 
 pRstTitles->Open ("Titles", _variant_t((IDispatch *) pConnection, 
 true), adOpenStatic, adLockOptimistic, adCmdTable); 
 
 // Print report of original data. 
 printf( 
 "\n\nData in Titles table before executing the query: \n"); 
 
 // Call function to print loop recordset contents. 
 PrintOutput(pRstTitles); 
 
 // Clear extraneous errors from the Errors collection. 
 pConnection->Errors->Clear(); 
 
 // Call ExecuteCommand subroutine to execute pCmdChange command. 
 ExecuteCommand(pCmdChange, pRstTitles); 
 
 // Print report of new data. 
 printf( 
 "\n\n\tData in Titles table after executing the query: \n"); 
 PrintOutput(pRstTitles); 
 
 // Use the Connection object's execute method to 
 // execute SQL statement to restore data. 
 pConnection->Execute(strSQLRestore, NULL, adExecuteNoRecords); 
 
 // Retrieve the current data by requerying the recordset. 
 pRstTitles->Requery(adCmdUnknown); 
 
 // Print report of restored data. 
 printf( 
 "\n\n\tData after exec. query to restore original info: \n"); 
 PrintOutput(pRstTitles); 
 } 
 catch (_com_error &e) 
 { 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRstTitles) 
 if (pRstTitles->State == adStateOpen) 
 pRstTitles->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////// 
// ExecuteCommand Function // 
////////////////////////////////////////// 
 
void ExecuteCommand(_CommandPtr pCmdTemp, _RecordsetPtr pRstTemp) 
{ 
 try 
 { 
 // CommandText property already set before function was called. 
 pCmdTemp->Execute(NULL, NULL, adCmdText); 
 
 // Retrieve the current data by requerying the recordset. 
 pRstTemp->Requery(adCmdUnknown); 
 } 
 
 catch(_com_error &e) 
 { 
 // Notify user of any errors that result from 
 // executing the query. 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(pRstTemp->GetActiveConnection()); 
 PrintComError(e); 
 } 
} 
 
///////////////////////////////////// 
// PrintOutput Function // 
///////////////////////////////////// 
 
void PrintOutput(_RecordsetPtr pRstTemp) 
{ 
 // Ensure at top of recordset. 
 pRstTemp->MoveFirst(); 
 
 // If EOF is true, then no data and skip print loop. 
 if( pRstTemp->EndOfFile ) 
 { 
 printf("\tRecordset empty\n"); 
 } 
 else 
 { 
 // Define temporary strings for output conversions. 
 // Initialize to first record's values. 
 _bstr_t bstrTitle; 
 _bstr_t bstrType; 
 
 // Enumerate Recordset and print from each. 
 while(!(pRstTemp->EndOfFile)) 
 { 
 // Convert variant string to convertable string type. 
 bstrTitle = pRstTemp->Fields->GetItem("Title")->Value; 
 bstrType = pRstTemp->Fields->GetItem("Type")->Value; 
 printf("\t%s, %s \n", 
 (LPCSTR) bstrTitle, 
 (LPCSTR) bstrType); 
 
 pRstTemp->MoveNext(); 
 } 
 } 
} 
 
/////////////////////////////////////////////// 
// PrintProviderError Function // 
/////////////////////////////////////////////// 
 
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
 printf("\t Error number: %x\t%s", pErr->Number, 
 pErr->Description); 
 } 
 } 
} 
 
////////////////////////////////////// 
// PrintComError Function // 
////////////////////////////////////// 
 
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
// EndExecuteCpp 
```
