---
title: Inicializar um provedor de armazenamento com quebra PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Modificado pela última vez: 05 de outubro de 2012'
ms.openlocfilehash: c39f66917ecc080785b3a3e91506d3994427ca62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569075"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Inicializar um provedor de armazenamento com quebra PST

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para implementar um provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra, você deve inicializar o provedor de armazenamento com quebra PST usando a função **[MSProviderInit](msproviderinit.md)** como ponto de partida. Depois que a DLL do provedor é inicializada, a função **[MSGSERVICEENTRY](msgserviceentry.md)** configura o provedor de repositórios de PST com quebra. 
  
Neste tópico, a função **MSProviderInit** e a função **MSGSERVICEENTRY** são demonstrados usando exemplos de código a partir do provedor de repositório de PST quebrado automaticamente amostra. O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação. Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).
  
Depois de você ter inicializar um provedor de armazenamento de PST com quebra, você deve implementar funções para que o MAPI e o MAPI spooler podem efetuar logon em um provedor de armazenamento de mensagem. Para obter mais informações, consulte [Log em um provedor de armazenamento de PST quebrado automaticamente](logging-on-to-a-wrapped-pst-store-provider.md).
  
## <a name="initialization-routine"></a>Rotina de inicialização

Todos os provedores de repositório PST com quebra devem implementar a função **[MSProviderInit](msproviderinit.md)** como um ponto de partida para inicializar a DLL do provedor. **MSProviderInit** verifica se o número de versão da interface do provedor de serviço, `ulMAPIVer`, é compatível com o número da versão atual, `CURRENT_SPI_VERSION`. A função salva a memória MAPI rotinas de gerenciamento para o `g_lpAllocateBuffer`, `g_lpAllocateMore`, e `g_lpFreeBuffer` parâmetros. Essas rotinas de gerenciamento de memória devem ser usadas em toda a implementação de repositório PST com quebra para desalocação e alocação de memória. 
  
### <a name="msproviderinit-example"></a>Exemplo de MSProviderInit()

```cpp
STDINITMETHODIMP MSProviderInit ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPALLOCATEBUFFER lpAllocateBuffer, 
    LPALLOCATEMORE lpAllocateMore, 
    LPFREEBUFFER lpFreeBuffer, 
    ULONG ulFlags, 
    ULONG ulMAPIVer, 
    ULONG FAR * lpulProviderVer, 
    LPMSPROVIDER FAR * lppMSProvider) 
{ 
    Log(true,"MSProviderInit function called\n"); 
    if (!lppMSProvider || !lpulProviderVer) return MAPI_E_INVALID_PARAMETER; 
    HRESULT hRes = S_OK; 
 
    *lppMSProvider = NULL; 
    *lpulProviderVer = CURRENT_SPI_VERSION; 
    if (ulMAPIVer < CURRENT_SPI_VERSION) 
    { 
        Log(true,"MSProviderInit: The version of the subsystem cannot handle this" 
            + "version of the provider\n"); 
        return MAPI_E_VERSION; 
    } 
 
    Log(true,"MSProviderInit: saving off memory management routines\n"); 
    g_lpAllocateBuffer = lpAllocateBuffer; 
    g_lpAllocateMore = lpAllocateMore; 
    g_lpFreeBuffer = lpFreeBuffer; 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true,"LoadLibrary returned 0x%08X\n", hm); 
 
    LPMSPROVIDERINIT pMsProviderInit = NULL; 
    if (hm) 
    { 
        pMsProviderInit = (LPMSPROVIDERINIT)GetProcAddress(hm, "MSProviderInit"); 
        Log(true,"GetProcAddress returned 0x%08X\n", pMsProviderInit); 
    } 
    else hRes = E_OUTOFMEMORY; 
    if (pMsProviderInit) 
    { 
        Log(true,"Calling pMsProviderInit\n"); 
        CMSProvider* pWrappedProvider = NULL; 
        LPMSPROVIDER pSyncProviderObj = NULL; 
        hRes = pMsProviderInit( 
            hm,// not hInstance: first param is handle of module in which the function lives 
            lpMalloc, 
            lpAllocateBuffer, 
            lpAllocateMore, 
            lpFreeBuffer, 
            ulFlags, 
            ulMAPIVer, 
            lpulProviderVer, 
            &pSyncProviderObj                         
            ); 
        Log(true,"pMsProviderInit returned 0x%08X\n", hRes); 
        if (SUCCEEDED(hRes)) 
        { 
            pWrappedProvider = new CMSProvider (pSyncProviderObj); 
            if (NULL == pWrappedProvider) 
            { 
                Log(true,"MSProviderInit: Failed to allocate new CMSProvider object\n"); 
                hRes = E_OUTOFMEMORY; 
            } 
            // Copy pointer to the allocated object back into the  
            //return IMSProvider object pointer 
            *lppMSProvider = pWrappedProvider; 
        } 
    } 
    else hRes = E_OUTOFMEMORY; 
    return hRes; 
}
```

### <a name="wrapped-pst-and-unicode-paths"></a>Caminhos com quebra de PST e Unicode

Para adaptar o exemplo original preparado no Microsoft Visual Studio 2008 para usar caminhos de Unicode para o NST para uso em Unicode habilitado para o Microsoft Outlook 2010 e o Outlook 2013, a rotina **CreateStoreEntryID** , que produz o identificador de entrada, deve usar um formato para caminhos de ASCII e outro para caminhos de Unicode. Esses itens são representados como estruturas no exemplo a seguir. 
  
```cpp
typedef struct                              // short format
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // Full path to store (ASCII)
 } EIDMS;
// Unicode version of EIDMSW is an extension of EIDMS
// and szPath is always NULL
typedef struct                              // Long format to support Unicode path and name
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // ASCII path to store is always NULL
         WCHAR            wzPath[1];       // Full path to store (Unicode)
} EIDMSW;
```

> [!IMPORTANT]
> As diferenças nessas estruturas são dois bytes NULL antes de um caminho de Unicode. Se você precisar interpretar o identificador de entrada no "serviço entrada rotina" que segue, seria uma maneira de determinar se for esse o caso ou não converter conforme EIDMS em primeiro lugar, verifique se o szPath [0] é NULL. Se for, convertê-lo como EIDMSW. 
  
## <a name="service-entry-routine"></a>Rotina de entrada de serviço

A função **[MSGSERVICEENTRY](msgserviceentry.md)** é o ponto de entrada do serviço de mensagem em que o provedor de repositórios de PST com quebra está configurado. As chamadas de função `GetMemAllocRoutines()` para obter a memória MAPI rotinas de gerenciamento. A função usa a `lpProviderAdmin` parâmetro para localizar a seção de perfil para o provedor e define as propriedades no perfil. 
  
### <a name="serviceentry-example"></a>Exemplo de ServiceEntry()

```cpp
HRESULT STDAPICALLTYPE ServiceEntry ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR *lppMapiError) 
{ 
    if (!lpMAPISup || !lpProviderAdmin) return MAPI_E_INVALID_PARAMETER; 
    HRESULT         hRes = S_OK; 
    Log(true,"ServiceEntry function called\n"); 
    Log(true,"About to call NSTServiceEntry\n"); 
 
    if (MSG_SERVICE_INSTALL         == ulContext || 
        MSG_SERVICE_DELETE            == ulContext || 
        MSG_SERVICE_UNINSTALL        == ulContext || 
        MSG_SERVICE_PROVIDER_CREATE == ulContext || 
        MSG_SERVICE_PROVIDER_DELETE == ulContext) 
    { 
        // These contexts are not supported 
        return MAPI_E_NO_SUPPORT; 
    } 
 
    // Get memory routines 
    hRes = lpMAPISup-> 
        GetMemAllocRoutines(&g_lpAllocateBuffer,&g_lpAllocateMore,&g_lpFreeBuffer); 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true, "Got module 0x%08X\n", hm); 
    if (!hm) return E_OUTOFMEMORY; 
    LPMSGSERVICEENTRY pNSTServiceEntry =  
        (LPMSGSERVICEENTRY)GetProcAddress(hm, "NSTServiceEntry"); 
    Log(true, "Got procaddress  0x%08X\n", pNSTServiceEntry); 
    if (!pNSTServiceEntry) return E_OUTOFMEMORY; 
 
    // Get profile section 
    LPPROFSECT lpProfSect = NULL; 
    hRes = lpProviderAdmin-> 
        OpenProfileSection((LPMAPIUID) NULL, NULL, MAPI_MODIFY, &lpProfSect); 
    // Set passed in props into the profile 
    if (lpProps && cValues) 
    { 
        hRes = lpProfSect->SetProps(cValues,lpProps,NULL); 
    } 
    // Make sure there is a store path set 
    if (SUCCEEDED(hRes)) hRes = SetOfflineStoreProps(lpProfSect,ulUIParam); 
    ULONG            ulProfProps = 0; 
    LPSPropValue    lpProfProps = NULL; 
 
    // Evaluate props 
    hRes = lpProfSect->GetProps((LPSPropTagArray)&sptClientProps, 
                                fMapiUnicode, 
                                &ulProfProps, 
                                &lpProfProps); 
    if (SUCCEEDED(hRes)) 
    { 
        CSupport * pMySup = NULL; 
        pMySup = new CSupport(lpMAPISup, lpProfSect); 
        if (!pMySup) 
        { 
            Log(true,"MSProviderInit: Failed to allocate new CSupport object\n"); 
            hRes = E_OUTOFMEMORY; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            hRes = pNSTServiceEntry( 
                hm,  
                lpMalloc, 
                pMySup, 
                ulUIParam, 
                ulFlags, 
                ulContext, 
                ulProfProps, 
                lpProfProps, 
                NULL,//pAdminProvObj, //Don't pass this when creating an NST 
                lppMapiError); 
            if (SUCCEEDED(hRes)) 
            { 
                // Finish setting up the profile 
                hRes = InitStoreProps( 
                    lpMAPISup,  
                    lpProfSect,  
                    lpProviderAdmin); 
                hRes = lpProfSect->SaveChanges(KEEP_OPEN_READWRITE); 
            } 
        } 
    } 
    Log(true, "Ran pNSTServiceEntry 0x%08X\n", hRes); 
    MyFreeBuffer(lpProfProps); 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="see-also"></a>Confira também

- [Sobre o exemplo de provedor do repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
- [Instalar o provedor do repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Fazer logon em um provedor do repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Usar um provedor do repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
- [Desativar um provedor do repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

