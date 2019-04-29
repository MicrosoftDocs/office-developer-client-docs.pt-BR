---
title: Fazer logon em um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Última modificação: 02 de julho de 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408983"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="4637d-103">Fazer logon em um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4637d-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="4637d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4637d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4637d-105">Antes de poder fazer logon em MAPI em um provedor de repositório PST encapsulado, você deve inicializar e configurar o provedor de repositório de arquivos de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="4637d-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="4637d-106">Para obter mais informações, consulte [inicialização de um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4637d-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="4637d-107">Depois de inicializar e configurar um provedor de repositório PST encapsulado, você deve implementar duas rotinas de logon.</span><span class="sxs-lookup"><span data-stu-id="4637d-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="4637d-108">A função **[IMSProvider:: logon](imsprovider-logon.md)** faz logon em MAPI para o provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="4637d-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="4637d-109">A função **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** registra o spooler MAPI no provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="4637d-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="4637d-110">Neste tópico, a função **IMSProvider:: logon** e a função **IMSProvider:: SpoolerLogon** são demonstradas usando exemplos de código do provedor de repositório PST encapsulado de amostra.</span><span class="sxs-lookup"><span data-stu-id="4637d-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="4637d-111">O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="4637d-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="4637d-112">Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4637d-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="4637d-113">Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="4637d-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="4637d-114">Após MAPI e o spooler MAPI conectado ao provedor de repositório PST encapsulado, ele está pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="4637d-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="4637d-115">Para obter mais informações, consulte [usar um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4637d-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="4637d-116">Rotina de logon de MAPI</span><span class="sxs-lookup"><span data-stu-id="4637d-116">MAPI Logon routine</span></span>

<span data-ttu-id="4637d-117">Após a inicialização do provedor de repositório PST encapsulado, você deve implementar a função **[IMSProvider:: logon](imsprovider-logon.md)** para fazer logon no MAPI no repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="4637d-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="4637d-118">Essa função valida as credenciais do usuário e obtém as propriedades de configuração do provedor.</span><span class="sxs-lookup"><span data-stu-id="4637d-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="4637d-119">Você também deve implementar a `SetOLFIInOST` função para definir as informações de arquivo offline (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="4637d-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="4637d-120">**OLFI** é uma fila de estruturas de ID de longo prazo que é usada pelo provedor de repositório PST encapsulado para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline.</span><span class="sxs-lookup"><span data-stu-id="4637d-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="4637d-121">Por fim, a função **IMSProvider:: logon** retorna um objeto de repositório de mensagens que o spooler MAPI e os aplicativos cliente podem fazer logon `ppMDB` no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4637d-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="4637d-122">CMSProvider:: logon () exemplo</span><span class="sxs-lookup"><span data-stu-id="4637d-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="4637d-123">Rotina de logon do spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="4637d-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="4637d-124">Semelhante a **IMSProvider:: logon**, você deve implementar a função **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** para registrar o spooler MAPI no repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="4637d-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="4637d-125">Um objeto de repositório de mensagens que os aplicativos cliente e spooler MAPI podem fazer logon é retornado no `ppMDB` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4637d-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="4637d-126">Exemplo de CMSProvider:: SpoolerLogon ()</span><span class="sxs-lookup"><span data-stu-id="4637d-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4637d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4637d-127">See also</span></span>

- [<span data-ttu-id="4637d-128">Sobre o exemplo de provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4637d-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="4637d-129">Instalando o provedor de repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="4637d-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="4637d-130">Inicializando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4637d-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="4637d-131">Usando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4637d-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="4637d-132">DesLigamento de um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4637d-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

