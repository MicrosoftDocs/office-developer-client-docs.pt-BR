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
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="74d07-103">Iniciar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="74d07-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="74d07-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74d07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74d07-105">Para implementar um provedor de armazenamento de pastas particulares (PST) empacotado, você deve inicializar o provedor de armazenamento PST empacotado usando a função **[MSProviderInit](msproviderinit.md)** como um ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="74d07-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="74d07-106">Depois que a DLL do provedor é inicializada, a **[função MSGSERVICEENTRY](msgserviceentry.md)** configura o provedor de armazenamento PST empacotado.</span><span class="sxs-lookup"><span data-stu-id="74d07-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="74d07-107">Neste tópico, as funções **MSProviderInit** e **MSGSERVICEENTRY** são demonstradas usando exemplos de código do Sample Wrapped PST Store Provider.</span><span class="sxs-lookup"><span data-stu-id="74d07-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="74d07-108">O exemplo implementa um provedor PST empacotado que se destina a ser usado em conjunto com a API de Replicação.</span><span class="sxs-lookup"><span data-stu-id="74d07-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="74d07-109">Para obter mais informações sobre como baixar e instalar o Sample Wrapped PST Store Provider, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="74d07-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="74d07-110">Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="74d07-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="74d07-111">Depois de inicializar um provedor de armazenamento PST empacotado, você deve implementar funções para que o MAPI e o spooler MAPI possam fazer logoff no provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="74d07-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="74d07-112">Para obter mais informações, consulte [Log On em um Provedor de Armazenamento PST empacotado.](logging-on-to-a-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="74d07-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="74d07-113">Rotina de inicialização</span><span class="sxs-lookup"><span data-stu-id="74d07-113">Initialization routine</span></span>

<span data-ttu-id="74d07-114">Todos os provedores de armazenamento PST empacotado devem implementar a **[função MSProviderInit](msproviderinit.md)** como um ponto de entrada para inicializar a DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="74d07-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="74d07-115">**MSProviderInit** verifica se o número de versão da interface do provedor de serviços, é compatível com o  `ulMAPIVer` número de versão atual,  `CURRENT_SPI_VERSION` .</span><span class="sxs-lookup"><span data-stu-id="74d07-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="74d07-116">A função salva as rotinas de gerenciamento de memória MAPI nos  `g_lpAllocateBuffer`  `g_lpAllocateMore` parâmetros ,  `g_lpFreeBuffer` e .</span><span class="sxs-lookup"><span data-stu-id="74d07-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="74d07-117">Essas rotinas de gerenciamento de memória devem ser usadas em toda a implementação do armazenamento PST empacotado para alocação e alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="74d07-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="74d07-118">Exemplo de MSProviderInit()</span><span class="sxs-lookup"><span data-stu-id="74d07-118">MSProviderInit() example</span></span>

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

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="74d07-119">Caminhos PST e Unicode empacotado</span><span class="sxs-lookup"><span data-stu-id="74d07-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="74d07-120">Para retroajustar o exemplo original preparado no Microsoft Visual Studio 2008 para usar caminhos Unicode para o NST para uso no Microsoft Outlook 2010 e Outlook 2013 habilitados para Unicode, a rotina **CreateStoreEntryID,** que produz o identificador de entrada, deve usar um formato para caminhos ASCII e outro para caminhos Unicode.</span><span class="sxs-lookup"><span data-stu-id="74d07-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="74d07-121">Eles são representados como estruturas no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="74d07-121">These are represented as structures in the following example.</span></span> 
  
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
> <span data-ttu-id="74d07-122">As diferenças nessas estruturas são dois bytes NULL antes de um caminho Unicode.</span><span class="sxs-lookup"><span data-stu-id="74d07-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="74d07-123">Se você precisar interpretar o identificador de entrada na "Rotina de Entrada de Serviço" a seguir, uma maneira de determinar se esse é o caso ou não seria lançar como EIDMS primeiro e, em seguida, verificar se o szPath[0] é NULL.</span><span class="sxs-lookup"><span data-stu-id="74d07-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="74d07-124">Se estiver, cast it as EIDMSW instead.</span><span class="sxs-lookup"><span data-stu-id="74d07-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="74d07-125">Rotina de entrada de serviço</span><span class="sxs-lookup"><span data-stu-id="74d07-125">Service Entry routine</span></span>

<span data-ttu-id="74d07-126">A **[função MSGSERVICEENTRY](msgserviceentry.md)** é o ponto de entrada do serviço de mensagens onde o provedor de armazenamento PST empacotado está configurado.</span><span class="sxs-lookup"><span data-stu-id="74d07-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="74d07-127">A função chama  `GetMemAllocRoutines()` para obter as rotinas de gerenciamento de memória MAPI.</span><span class="sxs-lookup"><span data-stu-id="74d07-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="74d07-128">A função usa o parâmetro para localizar a seção de perfil do  `lpProviderAdmin` provedor e define as propriedades no perfil.</span><span class="sxs-lookup"><span data-stu-id="74d07-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="74d07-129">Exemplo de ServiceEntry()</span><span class="sxs-lookup"><span data-stu-id="74d07-129">ServiceEntry() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="74d07-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="74d07-130">See also</span></span>

- [<span data-ttu-id="74d07-131">Sobre o provedor de armazenamento PST com conteúdo de exemplo</span><span class="sxs-lookup"><span data-stu-id="74d07-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="74d07-132">Instalando o provedor de armazenamento PST com conteúdo de exemplo</span><span class="sxs-lookup"><span data-stu-id="74d07-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="74d07-133">Fazendo logom em um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="74d07-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="74d07-134">Usando um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="74d07-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="74d07-135">Desligar um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="74d07-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

