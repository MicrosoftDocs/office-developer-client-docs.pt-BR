---
title: Fazer logon em um provedor de armazenamento com quebra PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 0716017788239c22f31007438089118d109010a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570475"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Fazer logon em um provedor de armazenamento com quebra PST

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes que você possa fazer logon MAPI para um provedor de armazenamento com quebra PST, você deve inicializar e configurar o provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra. Para obter mais informações, consulte [inicializar um provedor de armazenamento de PST quebrado automaticamente](initializing-a-wrapped-pst-store-provider.md).
  
Depois de ter inicializado e configurado um provedor de armazenamento com quebra PST, você deve implementar duas rotinas de logon. A função **[IMSProvider::Logon](imsprovider-logon.md)** faz logon MAPI para o provedor de repositórios de PST com quebra. A função **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** faz logon o spooler MAPI para o provedor de repositórios de PST com quebra. 
  
Neste tópico, a função **IMSProvider::Logon** e a função de **IMSProvider::SpoolerLogon** são demonstrados usando exemplos de código a partir do provedor de repositório de PST quebrado automaticamente amostra. O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação. Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).
  
Depois de MAPI e o spooler MAPI são registrados no arquivo PST com quebra o provedor de armazenamento, ele está pronto para ser usado. Para obter mais informações, consulte [usando um provedor de armazenamento de PST quebrado automaticamente](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Rotina de Logon MAPI

Depois que o provedor de repositórios de PST com quebra é inicializado, você deve implementar a função **[IMSProvider::Logon](imsprovider-logon.md)** fazer logon MAPI para o repositório PST encapsulado. Esta função valida credenciais de usuário e obtém as propriedades de configuração para o provedor. Você também deve implementar o `SetOLFIInOST` função para definir o Offline File Info (**[OLFI](olfi.md)** ). **OLFI** é uma fila de estruturas de ID de longo prazo que é usada pelo provedor de repositório PST com quebra para atribuir uma ID de entrada para uma nova mensagem ou a pasta no modo offline. Finalmente, a função **IMSProvider::Logon** retorna um objeto de repositório de mensagem que os aplicativos de cliente e o spooler MAPI podem fazer logon no `ppMDB` parâmetro. 
  
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

## <a name="mapi-spooler-logon-routine"></a>Rotina de Logon do MAPI Spooler

Semelhante ao **IMSProvider::Logon**, você deve implementar a função **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** para registrar o spooler MAPI para o repositório PST encapsulado. Um objeto de repositório de mensagem que os aplicativos de cliente e o spooler MAPI podem efetuar logon em é retornado no `ppMDB` parâmetro. 
  
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

- [Sobre o exemplo de provedor do repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md) 
- [Instalar o provedor do repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md) 
- [Iniciar um provedor do repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
- [Usar um provedor do repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
- [Desativar um provedor do repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

