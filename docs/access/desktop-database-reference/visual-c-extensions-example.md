---
title: Exemplo de extensões do Visual C++
TOCTitle: Visual C++ Extensions Example
ms:assetid: fe57868f-5707-3c5b-cb93-4121732d67cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250305(v=office.15)
ms:contentKeyID: 48548934
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f7bbcdc4f3ddcadfd45ba627873945ec1a3adfe
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946906"
---
# <a name="visual-c-extensions-example"></a><span data-ttu-id="6df29-102">Exemplo de Extensões do Visual C++</span><span class="sxs-lookup"><span data-stu-id="6df29-102">Visual C++ Extensions example</span></span>


<span data-ttu-id="6df29-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6df29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6df29-104">Este programa mostra como os valores são recuperados dos campos e convertidos em variáveis C/C++.</span><span class="sxs-lookup"><span data-stu-id="6df29-104">This program shows how values are retrieved from fields and converted to C/C++ variables.</span></span>

<span data-ttu-id="6df29-105">Este exemplo também tira vantagem do "ponteiros inteligentes", que lidam automaticamente os detalhes específicos do COM de chamada e para a interface **IADORecordBinding** de contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="6df29-105">This example also takes advantage of "smart pointers," which automatically handle the COM-specific details of calling and reference counting for the **IADORecordBinding** interface.</span></span>

<span data-ttu-id="6df29-106">Sem os ponteiros inteligentes, o código seria:</span><span class="sxs-lookup"><span data-stu-id="6df29-106">Without smart pointers, you would code:</span></span>

```cpp 
 
IADORecordBinding *picRs = NULL; 
... 
TESTHR(pRs->QueryInterface( 
 __uuidof(IADORecordBinding), (LPVOID*)&picRs)); 
... 
if (picRs) picRs->Release(); 
```

<span data-ttu-id="6df29-107">Com os ponteiros inteligentes, você deriva o tipo de IADORecordBindingPtr do tipo da interface IADORecordBinding com esta instrução:</span><span class="sxs-lookup"><span data-stu-id="6df29-107">With smart pointers, you derive the IADORecordBindingPtr type from the type from the IADORecordBinding interface with this statement:</span></span>

```cpp 
 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
```

<span data-ttu-id="6df29-108">E instancia o ponteiro da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6df29-108">And instantiate the pointer like this:</span></span>

```cpp 
 
IADORecordBindingPtr picRs(pRs); 
```

<span data-ttu-id="6df29-109">Porque as extensões do Visual C++ são implementadas pelo objeto **Recordset** , o construtor do ponteiro inteligente, picRs, utiliza o \_RecordsetPtr ponteiro, pRs.</span><span class="sxs-lookup"><span data-stu-id="6df29-109">Because the Visual C++ Extensions are implemented by the **Recordset** object, the constructor for the smart pointer, picRs , takes the \_RecordsetPtr pointer, pRs .</span></span> <span data-ttu-id="6df29-110">O construtor chama QueryInterface usando pRs para localizar a, usa o \_RecordsetPtr ponteiro, pRs.</span><span class="sxs-lookup"><span data-stu-id="6df29-110">The constructor calls QueryInterface using pRs to find the , takes the \_RecordsetPtr pointer, pRs .</span></span> <span data-ttu-id="6df29-111">O construtor chama QueryInterface usando pRs para localizar a interface IADORecordBinding.</span><span class="sxs-lookup"><span data-stu-id="6df29-111">The constructor calls QueryInterface using pRs to find the IADORecordBinding interface.</span></span>

```cpp 
 
// Visual C++ Extensions Example 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <stdio.h> 
#include <icrsint.h> 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
 
inline void TESTHR(HRESULT _hr) { if FAILED(_hr) _com_issue_error(_hr); } 
 
class CCustomRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CCustomRs) 
 ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_ch_fname, 
 sizeof(m_ch_fname), m_ul_fnameStatus, false) 
 ADO_VARIABLE_LENGTH_ENTRY2(4, adVarChar, m_ch_lname, 
 sizeof(m_ch_lname), m_ul_lnameStatus, false) 
END_ADO_BINDING() 
public: 
 CHAR m_ch_fname[22]; 
 CHAR m_ch_lname[32]; 
 ULONG m_ul_fnameStatus; 
 ULONG m_ul_lnameStatus; 
}; 
 
void main(void) 
{ 
 ::CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 CCustomRs rs; 
 IADORecordBindingPtr picRs(pRs); 
 
 pRs->Open("SELECT * FROM Employee ORDER BY lname", 
 "dsn=pubs;uid=sa;pwd=;", 
 adOpenStatic, adLockOptimistic, adCmdText); 
 
 TESTHR(picRs->BindToRecordset(&rs)); 
 
 while (!pRs->EndOfFile) 
 { 
 // Process data in the CCustomRs C++ instance variables. 
 printf("Name = %s %s\n", 
 (rs.m_ul_fnameStatus == adFldOK ? rs.m_ch_fname: "<Error>"), 
 (rs.m_ul_lnameStatus == adFldOK ? rs.m_ch_lname: "<Error>")); 
 
 // Move to the next row of the Recordset. 
 // Fields in the new row will automatically be 
 // placed in the CCustomRs C++ instance variables. 
 
 pRs->MoveNext(); 
 } 
 } 
 catch (_com_error &e ) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Meaning = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 } 
 ::CoUninitialize(); 
} 
```

