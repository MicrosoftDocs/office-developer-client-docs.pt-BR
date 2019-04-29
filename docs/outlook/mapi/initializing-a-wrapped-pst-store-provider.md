---
title: Iniciar um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Última modificação: 5 de outubro de 2012'
ms.openlocfilehash: 31114e4082fbc5e4c57da95eb6b32339822b1645
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427819"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Iniciar um provedor do repositório PST encapsulado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para implementar um provedor de repositório de arquivos de pastas particulares (PST) encapsulado, você deve inicializar o provedor de repositório PST encapsulado usando a função **[MSProviderInit](msproviderinit.md)** como ponto de entrada. Após a inicialização da DLL do provedor, a função **[MSGSERVICEENTRY](msgserviceentry.md)** configura o provedor de repositório PST encapsulado. 
  
Neste tópico, a função **MSProviderInit** e a função **MSGSERVICEENTRY** são demonstradas usando exemplos de código do provedor de repositório PST encapsulado de amostra. O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação. Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).
  
Depois de inicializar um provedor de repositório PST encapsulado, você deve implementar as funções para que o MAPI e o spooler MAPI possam fazer logon no provedor de armazenamento de mensagens. Para obter mais informações, consulte [fazendo logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md).
  
## <a name="initialization-routine"></a>Rotina de inicialização

Todos os provedores de repositório PST encapsulados devem implementar a função **[MSProviderInit](msproviderinit.md)** como ponto de entrada para inicializar a DLL do provedor. **MSProviderInit** verifica se o número da versão da interface `ulMAPIVer`do provedor de serviços é compatível com o número da versão atual. `CURRENT_SPI_VERSION` A função salva as rotinas de gerenciamento de memória `g_lpAllocateBuffer`MAPI `g_lpAllocateMore`nos parâmetros `g_lpFreeBuffer` , e. Essas rotinas de gerenciamento de memória devem ser usadas em toda a implementação do repositório PST encapsulado para alocação e desalocação de memória. 
  
### <a name="msproviderinit-example"></a>Exemplo de MSProviderInit ()

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

### <a name="wrapped-pst-and-unicode-paths"></a>Caminhos PST e Unicode encapsulados

Para adaptar o exemplo original preparado no Microsoft Visual Studio 2008 para usar caminhos Unicode para o NST para uso no Microsoft Outlook 2010 e no Outlook 2013 habilitado para Unicode, a rotina **CreateStoreEntryID** , que produz o identificador de entrada, deve usar um formato para caminhos ASCII e outro para caminhos Unicode. Eles são representados como estruturas no exemplo a seguir. 
  
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
> As diferenças nessas estruturas são dois bytes nulos antes de um caminho Unicode. Se você precisar interpretar o identificador de entrada na "rotina de entrada de serviço" que segue, uma maneira de determinar se esse é o caso ou não seria ser convertido como EIDMS primeiro e, em seguida, verifique se o szPath [0] é nulo. Se for, convertê-lo como EIDMSW em vez disso. 
  
## <a name="service-entry-routine"></a>Rotina de entrada de serviço

A função **[MSGSERVICEENTRY](msgserviceentry.md)** é o ponto de entrada do serviço de mensagens onde o provedor de repositório PST encapsulado está configurado. As chamadas `GetMemAllocRoutines()` de função para obter as rotinas de gerenciamento de memória MAPI. A função usa o `lpProviderAdmin` parâmetro para localizar a seção de perfil para o provedor e define as propriedades no perfil. 
  
### <a name="serviceentry-example"></a>Exemplo de userEntry ()

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

- [Sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
- [Instalando o provedor de repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
- [DesLigamento de um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

