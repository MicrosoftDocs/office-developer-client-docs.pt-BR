---
title: Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 039b3a45-bd57-51f5-1485-a3f6d1bde85a
description: Este tópico mostra como ler a estrutura TZDEFINITION do formato persistente armazenado em uma propriedade binária.
ms.openlocfilehash: a685fbfcf918e13aa82ac32799997bb05730184e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434204"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzdefinition-structure"></a><span data-ttu-id="51a99-103">Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="51a99-103">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>

<span data-ttu-id="51a99-104">Este tópico mostra como ler a estrutura [TZDEFINITION](tzdefinition.md) do formato persistente armazenado em uma propriedade binária.</span><span class="sxs-lookup"><span data-stu-id="51a99-104">This topic shows how to read the [TZDEFINITION](tzdefinition.md) structure from the persisted format stored in a binary property.</span></span> 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &amp;lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
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
 
    // We only understand if &amp;gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &amp;gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp;amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &amp;lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp;amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &amp;lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &amp;lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &amp;lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```

## <a name="see-also"></a><span data-ttu-id="51a99-105">Confira também</span><span class="sxs-lookup"><span data-stu-id="51a99-105">See also</span></span>

- [<span data-ttu-id="51a99-106">Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária</span><span class="sxs-lookup"><span data-stu-id="51a99-106">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [<span data-ttu-id="51a99-107">Ler propriedades de fuso horário de um compromisso</span><span class="sxs-lookup"><span data-stu-id="51a99-107">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

