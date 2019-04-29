---
title: Obter uma mensagem de contato com uma entrada do catálogo de endereços de contatos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Última modificação: 13 de agosto de 2013'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437788"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Obter uma mensagem de contato com uma entrada do catálogo de endereços de contatos

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo em C++, `HrOpenContact`que mostra como usar a estrutura [CONTAB_ENTRYID](contab_entryid.md) que identifica uma entrada em um catálogo de endereços de contatos para obter a mensagem de contato MAPI associada. 
  
`HrOpenContact`o tem os seguintes parâmetros: 
  
-  *lpSession* é um parâmetro de entrada que representa a sessão atual. **LPMAPISESSION** é definido no arquivo de cabeçalho MAPI mapix. h como um ponteiro para [IMAPISession: IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID* é um parâmetro de entrada que representa o tamanho do identificador de entrada associado ao *lpEntryID* . 
    
-  *lpEntryID* é um parâmetro de entrada que representa um ponteiro para o identificador de entrada de uma entrada em um catálogo de endereços de contatos. 
    
-  *parâmetroulflags* é um parâmetro de entrada que representa uma bitmask contendo sinalizadores de acesso a objetos à mensagem de contato MAPI. 
    
-  *lpContactMessage* é um parâmetro de saída que representa um ponteiro para a mensagem de contato MAPI. 
    
Para abrir a mensagem de contato MAPI subjacente `HrOpenContact` , o primeiro converte *lpEntryID* em um ponteiro para **CONTAB_ENTRYID**. Em seguida, ele chama [IMAPISession:: OpenEntry](imapisession-openentry.md) para obter a mensagem de contato MAPI, passando como parâmetros os campos *cbeid* e *Abeid* da entrada no catálogo de endereços de contatos que identificam, respectivamente, o tamanho do identificador de entrada e o identificador de entrada da mensagem de contato MAPI. 
  
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

