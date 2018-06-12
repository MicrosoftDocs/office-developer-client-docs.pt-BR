---
title: Fazer logon em um provedor de armazenamento com quebra PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 2dfa3820d8d2ab57f278e90bef5d5a40164da6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767762"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="c93eb-103">Fazer logon em um provedor de armazenamento com quebra PST</span><span class="sxs-lookup"><span data-stu-id="c93eb-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="c93eb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c93eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c93eb-105">Antes que você possa fazer logon MAPI para um provedor de armazenamento com quebra PST, você deve inicializar e configurar o provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra.</span><span class="sxs-lookup"><span data-stu-id="c93eb-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="c93eb-106">Para obter mais informações, consulte [inicializar um provedor de armazenamento de PST quebrado automaticamente](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c93eb-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="c93eb-107">Depois de ter inicializado e configurado um provedor de armazenamento com quebra PST, você deve implementar duas rotinas de logon.</span><span class="sxs-lookup"><span data-stu-id="c93eb-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="c93eb-108">A função **[IMSProvider::Logon](imsprovider-logon.md)** faz logon MAPI para o provedor de repositórios de PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="c93eb-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="c93eb-109">A função **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** faz logon o spooler MAPI para o provedor de repositórios de PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="c93eb-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="c93eb-110">Neste tópico, a função **IMSProvider::Logon** e a função de **IMSProvider::SpoolerLogon** são demonstrados usando exemplos de código a partir do provedor de repositório de PST quebrado automaticamente amostra.</span><span class="sxs-lookup"><span data-stu-id="c93eb-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="c93eb-111">O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="c93eb-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="c93eb-112">Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c93eb-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="c93eb-113">Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="c93eb-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="c93eb-114">Depois de MAPI e o spooler MAPI são registrados no arquivo PST com quebra o provedor de armazenamento, ele está pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="c93eb-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="c93eb-115">Para obter mais informações, consulte [usando um provedor de armazenamento de PST quebrado automaticamente](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c93eb-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="c93eb-116">Rotina de Logon MAPI</span><span class="sxs-lookup"><span data-stu-id="c93eb-116">MAPI Logon routine</span></span>

<span data-ttu-id="c93eb-117">Depois que o provedor de repositórios de PST com quebra é inicializado, você deve implementar a função **[IMSProvider::Logon](imsprovider-logon.md)** fazer logon MAPI para o repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="c93eb-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="c93eb-118">Esta função valida credenciais de usuário e obtém as propriedades de configuração para o provedor.</span><span class="sxs-lookup"><span data-stu-id="c93eb-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="c93eb-119">Você também deve implementar o `SetOLFIInOST` função para definir o Offline File Info (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="c93eb-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="c93eb-120">**OLFI** é uma fila de estruturas de ID de longo prazo que é usada pelo provedor de repositório PST com quebra para atribuir uma ID de entrada para uma nova mensagem ou a pasta no modo offline.</span><span class="sxs-lookup"><span data-stu-id="c93eb-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="c93eb-121">Finalmente, a função **IMSProvider::Logon** retorna um objeto de repositório de mensagem que os aplicativos de cliente e o spooler MAPI podem fazer logon no `ppMDB` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c93eb-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="c93eb-122">Exemplo de CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="c93eb-122">CMSProvider::Logon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="c93eb-123">Rotina de Logon do MAPI Spooler</span><span class="sxs-lookup"><span data-stu-id="c93eb-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="c93eb-124">Semelhante ao **IMSProvider::Logon**, você deve implementar a função **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** para registrar o spooler MAPI para o repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="c93eb-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="c93eb-125">Um objeto de repositório de mensagem que os aplicativos de cliente e o spooler MAPI podem efetuar logon em é retornado no `ppMDB` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c93eb-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="c93eb-126">Exemplo de CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="c93eb-126">CMSProvider::SpoolerLogon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="c93eb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c93eb-127">See also</span></span>

- [<span data-ttu-id="c93eb-128">Sobre a amostra quebradas provedor de repositórios de PST</span><span class="sxs-lookup"><span data-stu-id="c93eb-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="c93eb-129">Instalação do exemplo quebrado automaticamente o provedor de armazenamento de PST</span><span class="sxs-lookup"><span data-stu-id="c93eb-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="c93eb-130">Inicializar um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="c93eb-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="c93eb-131">Usando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="c93eb-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="c93eb-132">Encerrando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="c93eb-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

