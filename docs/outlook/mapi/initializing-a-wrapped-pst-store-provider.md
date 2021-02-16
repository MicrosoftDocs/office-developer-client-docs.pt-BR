---
title: Iniciar um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Last modified: October 05, 2012'
ms.openlocfilehash: 31114e4082fbc5e4c57da95eb6b32339822b1645
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427819"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Iniciar um provedor do repositório PST encapsulado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para implementar um provedor de armazenamento de pastas particulares (PST) empacotado, você deve inicializar o provedor de armazenamento PST empacotado usando a função **[MSProviderInit](msproviderinit.md)** como um ponto de entrada. Depois que a DLL do provedor é inicializada, a **[função MSGSERVICEENTRY](msgserviceentry.md)** configura o provedor de armazenamento PST empacotado. 
  
Neste tópico, as funções **MSProviderInit** e **MSGSERVICEENTRY** são demonstradas usando exemplos de código do Sample Wrapped PST Store Provider. O exemplo implementa um provedor PST empacotado que se destina a ser usado em conjunto com a API de Replicação. Para obter mais informações sobre como baixar e instalar o Sample Wrapped PST Store Provider, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)
  
Depois de inicializar um provedor de armazenamento PST empacotado, você deve implementar funções para que o MAPI e o spooler MAPI possam fazer logoff no provedor de armazenamento de mensagens. Para obter mais informações, consulte [Log On em um Provedor de Armazenamento PST empacotado.](logging-on-to-a-wrapped-pst-store-provider.md)
  
## <a name="initialization-routine"></a>Rotina de inicialização

Todos os provedores de armazenamento PST empacotado devem implementar a **[função MSProviderInit](msproviderinit.md)** como um ponto de entrada para inicializar a DLL do provedor. **MSProviderInit** verifica se o número de versão da interface do provedor de serviços, é compatível com o  `ulMAPIVer` número de versão atual,  `CURRENT_SPI_VERSION` . A função salva as rotinas de gerenciamento de memória MAPI nos  `g_lpAllocateBuffer`  `g_lpAllocateMore` parâmetros ,  `g_lpFreeBuffer` e . Essas rotinas de gerenciamento de memória devem ser usadas em toda a implementação do armazenamento PST empacotado para alocação e alocação de memória. 
  
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

### <a name="wrapped-pst-and-unicode-paths"></a>Caminhos PST e Unicode empacotado

Para retroajustar o exemplo original preparado no Microsoft Visual Studio 2008 para usar caminhos Unicode para o NST para uso no Microsoft Outlook 2010 e Outlook 2013 habilitados para Unicode, a rotina **CreateStoreEntryID,** que produz o identificador de entrada, deve usar um formato para caminhos ASCII e outro para caminhos Unicode. Eles são representados como estruturas no exemplo a seguir. 
  
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
> As diferenças nessas estruturas são dois bytes NULL antes de um caminho Unicode. Se você precisar interpretar o identificador de entrada na "Rotina de Entrada de Serviço" a seguir, uma maneira de determinar se esse é o caso ou não seria lançar como EIDMS primeiro e, em seguida, verificar se o szPath[0] é NULL. Se estiver, cast it as EIDMSW instead. 
  
## <a name="service-entry-routine"></a>Rotina de entrada de serviço

A **[função MSGSERVICEENTRY](msgserviceentry.md)** é o ponto de entrada do serviço de mensagens onde o provedor de armazenamento PST empacotado está configurado. A função chama  `GetMemAllocRoutines()` para obter as rotinas de gerenciamento de memória MAPI. A função usa o parâmetro para localizar a seção de perfil do  `lpProviderAdmin` provedor e define as propriedades no perfil. 
  
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

- [Sobre o provedor de armazenamento PST com conteúdo de exemplo](about-the-sample-wrapped-pst-store-provider.md)
- [Instalando o provedor de armazenamento PST com conteúdo de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Fazendo logom em um provedor de armazenamento PST empacotado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Usando um provedor de armazenamento PST empacotado](using-a-wrapped-pst-store-provider.md)
- [Desligar um provedor de armazenamento PST empacotado](shutting-down-a-wrapped-pst-store-provider.md)

