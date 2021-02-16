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
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Fazer logon em um provedor do repositório PST encapsulado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de fazer logoff no MAPI para um provedor de armazenamento PST empacotado, você deve inicializar e configurar o provedor de armazenamento PST (arquivo de Pastas Particulares) empacotado. Para obter mais informações, consulte [Inicializando um provedor de armazenamento PST.](initializing-a-wrapped-pst-store-provider.md)
  
Depois de inicializar e configurar um provedor de armazenamento PST, você deve implementar duas rotinas de logon. A **[função IMSProvider::Logon](imsprovider-logon.md)** faz logon no MAPI para o provedor de armazenamento PST empacotado. A **[função IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** registra no spooler MAPI para o provedor de armazenamento PST empacotado. 
  
Neste tópico, a função **IMSProvider::Logon** e a função **IMSProvider::SpoolerLogon** são demonstradas usando exemplos de código do Sample Wrapped PST Store Provider. O exemplo implementa um provedor PST empacotado que se destina a ser usado em conjunto com a API de Replicação. Para obter mais informações sobre como baixar e instalar o Sample Wrapped PST Store Provider, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)
  
Depois que o MAPI e o spooler MAPI são conectados ao provedor de armazenamento PST disposto, ele está pronto para ser usado. Para obter mais informações, consulte [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Rotina de logon MAPI

Depois que o provedor de armazenamento PST empacotado for inicializado, você deverá implementar a função **[IMSProvider::Logon](imsprovider-logon.md)** para fazer logon no MAPI para o armazenamento PST empacotado. Essa função valida as credenciais do usuário e obtém as propriedades de configuração do provedor. Você também deve implementar a `SetOLFIInOST` função para definir as Informações do Arquivo Offline **[(OLFI).](olfi.md)** **O OLFI** é uma fila de estruturas de ID de longo prazo usada pelo provedor de armazenamento PST empacotado para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline. Por fim, a **função IMSProvider::Logon** retorna um objeto de armazenamento de mensagens em que o spooler MAPI e os aplicativos cliente podem fazer logon no  `ppMDB` parâmetro. 
  
### <a name="cmsproviderlogon-example"></a>Exemplo de CMSProvider::Logon()

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

## <a name="mapi-spooler-logon-routine"></a>Rotina de logon do Spooler MAPI

Semelhante a **IMSProvider::Logon**, você deve implementar a função **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** para fazer logon do spooler MAPI no armazenamento PST empacotado. Um objeto de armazenamento de mensagens no que o spooler MAPI e os aplicativos cliente podem fazer logoff é retornado no  `ppMDB` parâmetro. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Exemplo de CMSProvider::SpoolerLogon()

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

## <a name="see-also"></a>Confira também

- [Sobre o provedor de armazenamento PST com conteúdo de exemplo](about-the-sample-wrapped-pst-store-provider.md) 
- [Instalando o provedor de armazenamento PST com conteúdo de exemplo](installing-the-sample-wrapped-pst-store-provider.md) 
- [Inicializando um provedor de armazenamento PST empacotado](initializing-a-wrapped-pst-store-provider.md)
- [Usando um provedor de armazenamento PST empacotado](using-a-wrapped-pst-store-provider.md)
- [Desligar um provedor de armazenamento PST empacotado](shutting-down-a-wrapped-pst-store-provider.md)

