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
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Fazer logon em um provedor do repositório PST encapsulado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de poder fazer logon em MAPI em um provedor de repositório PST encapsulado, você deve inicializar e configurar o provedor de repositório de arquivos de pastas particulares (PST). Para obter mais informações, consulte [inicialização de um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md).
  
Depois de inicializar e configurar um provedor de repositório PST encapsulado, você deve implementar duas rotinas de logon. A função **[IMSProvider:: logon](imsprovider-logon.md)** faz logon em MAPI para o provedor de repositório PST encapsulado. A função **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** registra o spooler MAPI no provedor de repositório PST encapsulado. 
  
Neste tópico, a função **IMSProvider:: logon** e a função **IMSProvider:: SpoolerLogon** são demonstradas usando exemplos de código do provedor de repositório PST encapsulado de amostra. O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação. Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).
  
Após MAPI e o spooler MAPI conectado ao provedor de repositório PST encapsulado, ele está pronto para ser usado. Para obter mais informações, consulte [usar um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Rotina de logon de MAPI

Após a inicialização do provedor de repositório PST encapsulado, você deve implementar a função **[IMSProvider:: logon](imsprovider-logon.md)** para fazer logon no MAPI no repositório PST encapsulado. Essa função valida as credenciais do usuário e obtém as propriedades de configuração do provedor. Você também deve implementar a `SetOLFIInOST` função para definir as informações de arquivo offline (**[OLFI](olfi.md)** ). **OLFI** é uma fila de estruturas de ID de longo prazo que é usada pelo provedor de repositório PST encapsulado para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline. Por fim, a função **IMSProvider:: logon** retorna um objeto de repositório de mensagens que o spooler MAPI e os aplicativos cliente podem fazer logon `ppMDB` no parâmetro. 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider:: logon () exemplo

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

## <a name="mapi-spooler-logon-routine"></a>Rotina de logon do spooler MAPI

Semelhante a **IMSProvider:: logon**, você deve implementar a função **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** para registrar o spooler MAPI no repositório PST encapsulado. Um objeto de repositório de mensagens que os aplicativos cliente e spooler MAPI podem fazer logon é retornado no `ppMDB` parâmetro. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Exemplo de CMSProvider:: SpoolerLogon ()

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

- [Sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md) 
- [Instalando o provedor de repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md) 
- [Inicializando um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
- [Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
- [DesLigamento de um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

