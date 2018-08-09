---
title: Detectar a versão do Exchange Server em um perfil do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: 3ed3def3fd76ec4f67239958b5d5164d97f81d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766710"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a><span data-ttu-id="afa22-103">Detectar a versão do Exchange Server em um perfil do Outlook</span><span class="sxs-lookup"><span data-stu-id="afa22-103">Detect the version of Exchange Server in an Outlook profile</span></span>

<span data-ttu-id="afa22-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afa22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afa22-105">Este tópico inclui um exemplo de código em C++ que mostra como usar a propriedade **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** e a propriedade **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** para obter informações sobre a versão do Microsoft Exchange Server que é a conta do active conectado ao.</span><span class="sxs-lookup"><span data-stu-id="afa22-105">This topic includes a code sample in C++ that shows how to use the **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** property and **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** property to obtain version information of the Microsoft Exchange Server that the active account is connected to.</span></span> 
  
<span data-ttu-id="afa22-106">O `GetProfileServiceVersion` função na amostra de código aceita um perfil como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="afa22-106">The  `GetProfileServiceVersion` function in the code sample accepts a profile as an input parameter.</span></span> <span data-ttu-id="afa22-107">Dependendo se a propriedade **PR_PROFILE_SERVER_VERSION** e a propriedade **PR_PROFILE_SERVER_FULL_VERSION** existirem no perfil determinado, a função obtém cada propriedade e retorna as informações de versão apropriada como saída parâmetros.</span><span class="sxs-lookup"><span data-stu-id="afa22-107">Depending on whether the **PR_PROFILE_SERVER_VERSION** property and the **PR_PROFILE_SERVER_FULL_VERSION** property exist in the given profile, the function gets each property and returns the appropriate version information as output parameters.</span></span> 
  
<span data-ttu-id="afa22-108">`GetProfileServiceVersion`Primeiramente, chama a função **[MAPIAdminProfiles](mapiadminprofiles.md)** para criar um objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="afa22-108">`GetProfileServiceVersion` first calls the **[MAPIAdminProfiles](mapiadminprofiles.md)** function to create a profile administration object.</span></span> <span data-ttu-id="afa22-109">Ele usa o objeto de administração de perfil para chamar **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** para obter um objeto de administração do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="afa22-109">It then uses the profile administration object to call **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** to obtain a message service administration object.</span></span> <span data-ttu-id="afa22-110">Usando o objeto de administração do serviço de mensagem, ele chama **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** para obter uma seção do perfil atual e, em seguida, chama **[HrGetOneProp](hrgetoneprop.md)** para verificar se cada uma das duas propriedades existe na seção do perfil e, em seguida, em caso afirmativo, define as informações de versão nos parâmetros de saída apropriada.</span><span class="sxs-lookup"><span data-stu-id="afa22-110">Using the message service administration object, it calls **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** to obtain a section of the current profile, and then calls **[HrGetOneProp](hrgetoneprop.md)** to verify if each of the two properties exists in that section of the profile, and if so, sets the version information in the appropriate output parameters.</span></span> 
  
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


