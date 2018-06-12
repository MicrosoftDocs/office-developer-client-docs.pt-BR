---
title: Obter uma mensagem de contato recebe uma entrada de catálogo de endereços de contatos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Modificado pela última vez: 13 de agosto de 2013'
ms.openlocfilehash: 346e6bc471f5257aacb34c2e7d02a0aade1bb46e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766733"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Obter uma mensagem de contato recebe uma entrada de catálogo de endereços de contatos

**Aplica-se a**: Outlook 
  
Este tópico contém um exemplo em C++, `HrOpenContact`, que mostra como usar a estrutura [CONTAB_ENTRYID](contab_entryid.md) que identifica uma entrada no catálogo de endereços de contatos para obter a mensagem de contato de MAPI associada. 
  
`HrOpenContact`tem os seguintes parâmetros: 
  
-  *lpSession* é um parâmetro de entrada que representa a sessão atual. **LPMAPISESSION** definida no mapix.h de arquivo de cabeçalho de MAPI como um ponteiro para [IMAPISession: IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID* é um parâmetro de entrada que representa o tamanho do identificador de entrada associado *lpEntryID* . 
    
-  *lpEntryID* é um parâmetro de entrada que representa um ponteiro para o identificador de entrada de uma entrada em um catálogo de endereços de contatos. 
    
-  *ulFlags* é um parâmetro de entrada que representa uma bitmask que contém os sinalizadores de objeto de acesso à mensagem de contato de MAPI. 
    
-  *lpContactMessage* é um parâmetro de saída que representa um ponteiro para a mensagem de contato de MAPI. 
    
Para abrir a mensagem subjacente do contato de MAPI, `HrOpenContact` primeiro projeta *lpEntryID* para um ponteiro para **CONTAB_ENTRYID**. Ela chama [IMAPISession::OpenEntry](imapisession-openentry.md) para obter a mensagem de contato de MAPI, passando como parâmetros os campos *cbeid* e *abeid* da entrada no catálogo de endereços de contatos que identificam, respectivamente, o tamanho do identificador de entrada e o Identificador de entrada da mensagem de contato de MAPI. 
  
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

## <a name="see-also"></a>Confira também

- [IMAPISession::OpenEntry](imapisession-openentry.md)

