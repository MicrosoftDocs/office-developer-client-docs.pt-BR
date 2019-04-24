---
title: Detectar a versão do Exchange Server em um perfil do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Última modificação: 03 de julho de 2012'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345539"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Detectar a versão do Exchange Server em um perfil do Outlook

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico inclui um exemplo de código em C++ que mostra como usar a propriedade **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** e a propriedade **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** para obter informações de versão do Microsoft Exchange Server que a conta ativa é conectado. 
  
A `GetProfileServiceVersion` função no exemplo de código aceita um perfil como um parâmetro de entrada. Dependendo se a propriedade **PR_PROFILE_SERVER_VERSION** e a propriedade **PR_PROFILE_SERVER_FULL_VERSION** existirem em um determinado perfil, a função obtém cada propriedade e retorna as informações da versão apropriada como saída parâmetros. 
  
`GetProfileServiceVersion`primeiro chama a função **[MAPIAdminProfiles](mapiadminprofiles.md)** para criar um objeto de administração de perfil. Em seguida, ele usa o objeto de administração de perfil para chamar **[IProfAdmin:: adminservices](iprofadmin-adminservices.md)** para obter um objeto de administração de serviço de mensagens. Usando o objeto de administração do serviço de mensagens, ele chama **[IMsgServiceAdmin:: OpenProfileSection](imsgserviceadmin-openprofilesection.md)** para obter uma seção do perfil atual e, em seguida, chama o **[HrGetOneProp](hrgetoneprop.md)** para verificar se cada uma das duas propriedades existe nessa seção do e, em caso afirmativo, define as informações de versão nos parâmetros de saída apropriados. 
  
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


