---
title: Fazer logon em um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408983"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="45fcf-103">Fazer logon em um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="45fcf-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="45fcf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45fcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45fcf-105">Antes de fazer logoff no MAPI para um provedor de armazenamento PST empacotado, você deve inicializar e configurar o provedor de armazenamento PST (arquivo de Pastas Particulares) empacotado.</span><span class="sxs-lookup"><span data-stu-id="45fcf-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="45fcf-106">Para obter mais informações, consulte [Inicializando um provedor de armazenamento PST.](initializing-a-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="45fcf-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="45fcf-107">Depois de inicializar e configurar um provedor de armazenamento PST, você deve implementar duas rotinas de logon.</span><span class="sxs-lookup"><span data-stu-id="45fcf-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="45fcf-108">A **[função IMSProvider::Logon](imsprovider-logon.md)** faz logon no MAPI para o provedor de armazenamento PST empacotado.</span><span class="sxs-lookup"><span data-stu-id="45fcf-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="45fcf-109">A **[função IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** registra no spooler MAPI para o provedor de armazenamento PST empacotado.</span><span class="sxs-lookup"><span data-stu-id="45fcf-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="45fcf-110">Neste tópico, a função **IMSProvider::Logon** e a função **IMSProvider::SpoolerLogon** são demonstradas usando exemplos de código do Sample Wrapped PST Store Provider.</span><span class="sxs-lookup"><span data-stu-id="45fcf-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="45fcf-111">O exemplo implementa um provedor PST empacotado que se destina a ser usado em conjunto com a API de Replicação.</span><span class="sxs-lookup"><span data-stu-id="45fcf-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="45fcf-112">Para obter mais informações sobre como baixar e instalar o Sample Wrapped PST Store Provider, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="45fcf-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="45fcf-113">Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="45fcf-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="45fcf-114">Depois que o MAPI e o spooler MAPI são conectados ao provedor de armazenamento PST disposto, ele está pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="45fcf-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="45fcf-115">Para obter mais informações, consulte [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="45fcf-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="45fcf-116">Rotina de logon MAPI</span><span class="sxs-lookup"><span data-stu-id="45fcf-116">MAPI Logon routine</span></span>

<span data-ttu-id="45fcf-117">Depois que o provedor de armazenamento PST empacotado for inicializado, você deverá implementar a função **[IMSProvider::Logon](imsprovider-logon.md)** para fazer logon no MAPI para o armazenamento PST empacotado.</span><span class="sxs-lookup"><span data-stu-id="45fcf-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="45fcf-118">Essa função valida as credenciais do usuário e obtém as propriedades de configuração do provedor.</span><span class="sxs-lookup"><span data-stu-id="45fcf-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="45fcf-119">Você também deve implementar a `SetOLFIInOST` função para definir as Informações do Arquivo Offline **[(OLFI).](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="45fcf-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="45fcf-120">**O OLFI** é uma fila de estruturas de ID de longo prazo usada pelo provedor de armazenamento PST empacotado para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline.</span><span class="sxs-lookup"><span data-stu-id="45fcf-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="45fcf-121">Por fim, a **função IMSProvider::Logon** retorna um objeto de armazenamento de mensagens em que o spooler MAPI e os aplicativos cliente podem fazer logon no  `ppMDB` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="45fcf-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="45fcf-122">Exemplo de CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="45fcf-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="45fcf-123">Rotina de logon do Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="45fcf-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="45fcf-124">Semelhante a **IMSProvider::Logon**, você deve implementar a função **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** para fazer logon do spooler MAPI no armazenamento PST empacotado.</span><span class="sxs-lookup"><span data-stu-id="45fcf-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="45fcf-125">Um objeto de armazenamento de mensagens no que o spooler MAPI e os aplicativos cliente podem fazer logoff é retornado no  `ppMDB` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="45fcf-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="45fcf-126">Exemplo de CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="45fcf-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="45fcf-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="45fcf-127">See also</span></span>

- [<span data-ttu-id="45fcf-128">Sobre o provedor de armazenamento PST com conteúdo de exemplo</span><span class="sxs-lookup"><span data-stu-id="45fcf-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="45fcf-129">Instalando o provedor de armazenamento PST com conteúdo de exemplo</span><span class="sxs-lookup"><span data-stu-id="45fcf-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="45fcf-130">Inicializando um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="45fcf-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="45fcf-131">Usando um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="45fcf-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="45fcf-132">Desligar um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="45fcf-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

