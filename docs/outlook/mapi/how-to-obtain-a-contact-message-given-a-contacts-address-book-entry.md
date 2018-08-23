---
title: Obter uma mensagem de contato recebe uma entrada de catálogo de endereços de contatos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Modificado pela última vez: 13 de agosto de 2013'
ms.openlocfilehash: 472b5847053c0a18026c76b8055a26551331d8dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564539"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="0b96a-103">Obter uma mensagem de contato recebe uma entrada de catálogo de endereços de contatos</span><span class="sxs-lookup"><span data-stu-id="0b96a-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="0b96a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b96a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b96a-105">Este tópico contém um exemplo em C++, `HrOpenContact`, que mostra como usar a estrutura [CONTAB_ENTRYID](contab_entryid.md) que identifica uma entrada no catálogo de endereços de contatos para obter a mensagem de contato de MAPI associada.</span><span class="sxs-lookup"><span data-stu-id="0b96a-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="0b96a-106">`HrOpenContact`tem os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="0b96a-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="0b96a-107">*lpSession* é um parâmetro de entrada que representa a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="0b96a-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="0b96a-108">**LPMAPISESSION** definida no mapix.h de arquivo de cabeçalho de MAPI como um ponteiro para [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0b96a-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="0b96a-109">*cbEntryID* é um parâmetro de entrada que representa o tamanho do identificador de entrada associado *lpEntryID* .</span><span class="sxs-lookup"><span data-stu-id="0b96a-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="0b96a-110">*lpEntryID* é um parâmetro de entrada que representa um ponteiro para o identificador de entrada de uma entrada em um catálogo de endereços de contatos.</span><span class="sxs-lookup"><span data-stu-id="0b96a-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="0b96a-111">*ulFlags* é um parâmetro de entrada que representa uma bitmask que contém os sinalizadores de objeto de acesso à mensagem de contato de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0b96a-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="0b96a-112">*lpContactMessage* é um parâmetro de saída que representa um ponteiro para a mensagem de contato de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0b96a-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="0b96a-113">Para abrir a mensagem subjacente do contato de MAPI, `HrOpenContact` primeiro projeta *lpEntryID* para um ponteiro para **CONTAB_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="0b96a-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="0b96a-114">Ela chama [IMAPISession::OpenEntry](imapisession-openentry.md) para obter a mensagem de contato de MAPI, passando como parâmetros os campos *cbeid* e *abeid* da entrada no catálogo de endereços de contatos que identificam, respectivamente, o tamanho do identificador de entrada e o Identificador de entrada da mensagem de contato de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0b96a-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```

## <a name="see-also"></a><span data-ttu-id="0b96a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b96a-115">See also</span></span>

- [<span data-ttu-id="0b96a-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0b96a-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)

