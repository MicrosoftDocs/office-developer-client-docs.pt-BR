---
<<<<<<< Título cabeça: TOCTitle de exemplo da propriedade StayInSync (VC + +): exemplo da propriedade StayInSync (VC + +) === título: exemplo da propriedade StayInSync (VC + +) TOCTitle: exemplo da propriedade StayInSync (VC + +)
>>>>>>> ms:assetid de mestre: 42c389a8-e6d5-45f4-0442-1b2a2422dcbe ms:mtpsurl: https://msdn.microsoft.com/library/JJ249197(v=office.15) ms:contentKeyID: ms.date 48544485: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="stayinsync-property-example-vc"></a>Exemplo da propriedade StayInSync (VC++)
=======
# <a name="stayinsync-property-example-vc"></a>Exemplo da propriedade StayInSync (VC + +)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Este exemplo demonstra como a propriedade [StayInSync](stayinsync-property-ado.md) facilita o acesso às linhas em um [Recordset](recordset-object-ado.md) hierárquico.

O loop externo exibe o nome e o sobrenome, o estado e a identificação de cada autor. O **Recordset** acrescentado em cada linha é recuperado da coleção [Fields](fields-collection-ado.md) e atribuído automaticamente a **rstTitleAuthor** pela propriedade **StayInSync** sempre que o **Recordset** pai se move para uma nova linha. O loop interno exibe quatro campos a partir de cada linha no conjunto de registros acrescentado.

```cpp 
 
// BeginStayInSyncCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void StayInSyncX(void); 
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
 
 StayInSyncX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// StayInSyncX Function // 
// // 
////////////////////////////////////////////////////////// 
void StayInSyncX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strCnn("Provider='MSDataShape';" 
 "Data Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 _RecordsetPtr pRst = NULL; 
 _RecordsetPtr pRstTitleAuthor = NULL; 
 
 try 
 { 
 TESTHR(pRstTitleAuthor.CreateInstance(__uuidof(Recordset))); 
 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 
 TESTHR(pRst.CreateInstance(__uuidof(Recordset))); 
 
 // Open connection. 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 pRst->PutStayInSync(true); 
 
 // Open recordset with names from Author & titleauthor table. 
 pRst->Open("SHAPE {select * from authors} " 
 "APPEND ({select * from titleauthor}" 
 "RELATE au_id TO au_id) AS chapTitleAuthor", 
 _variant_t((IDispatch*)pConnection,true), 
 adOpenStatic, adLockReadOnly, adCmdText); 
 
 pRstTitleAuthor = pRst->GetFields()->GetItem("chapTitleAuthor")-> 
 Value; 
 int intLineCnt=0; 
 while(!(pRst->EndOfFile)) 
 { 
 printf("\n%s %s %s %s\n", (LPCSTR)(_bstr_t)pRst-> 
 Fields->GetItem("au_fname")->Value, 
 (LPCSTR)(_bstr_t)pRst->Fields->GetItem("au_lname")->Value, 
 (LPCSTR)(_bstr_t)pRst->Fields->GetItem("state")->Value, 
 (LPCSTR)(_bstr_t)pRst->Fields->GetItem("au_id")->Value); 
 intLineCnt++; 
 
 if (intLineCnt%15 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 
 _variant_t vIndex; 
 while(!(pRstTitleAuthor->EndOfFile)) 
 { 
 vIndex = (short) 0; 
 printf("%s ",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 vIndex = (short) 1; 
 printf("%s ",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 vIndex = (short) 2; 
 printf("%s ",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 vIndex = (short) 3; 
 printf("%s\n",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 intLineCnt++; 
 
 if (intLineCnt%15 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 pRstTitleAuthor->MoveNext(); 
 } 
 pRst->MoveNext(); 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRst) 
 if (pRst->State == adStateOpen) 
 pRst->Close(); 
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
// EndStayInSyncCpp 
```

