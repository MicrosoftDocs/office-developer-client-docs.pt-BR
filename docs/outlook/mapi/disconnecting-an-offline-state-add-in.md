---
title: Desconectar-se de um suplemento de estado offline
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: ce25c6777c8a71da0fe11e0bbf34eefafe2ca50d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564133"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Desconectar-se de um suplemento de estado offline

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando o suplemento de estado offline estiver desconectado, você deve implementar funções para encerrar e limpar o suplemento corretamente. Para obter mais informações sobre como configurar e usar o offline estado suplemento para monitorar as alterações de estado de conexão, consulte [Add-in de configuração de backup de um estado Offline](setting-up-an-offline-state-add-in.md) e [Monitoramento Conexão estado alterações usando um suplemento do estado Offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
Neste tópico, esses desconexão, encerrar e funções de limpeza são demonstradas usando exemplos de código a partir do suplemento de amostra Offline estado. O suplemento de amostra Offline estado é um suplemento de COM que adiciona um menu de **Estado Offline** para o Outlook e usa a API de estado Offline. Através do menu de estado Offline, você pode habilitar ou desabilitar o monitoramento do estado, verifique o estado atual e alterar o estado atual. Para obter mais informações sobre como baixar e instalar o suplemento de amostra Offline estado, consulte [Instalando o suplemento de amostra Offline estado](installing-the-sample-offline-state-add-in.md). Para obter mais informações sobre a API de estado Offline, consulte [Sobre o Offline estado API](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Na rotina de desconexão

O método **IDTExtensibility2.OnDisconnection** é chamado quando o suplemento de estado Offline seja descarregado. Você deve implementar a limpeza do código nessa função. No exemplo a seguir, a função de **IDTExtensibility2.OnDisconnection** chama o `HrTermAddin` função. 
  
### <a name="cmyaddinondisconnection-example"></a>Exemplo de CMyAddin::OnDisconnection()

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Encerrar a função de suplemento

O `HrTermAddin` chamadas de função a `inDeInitMonitor`, `HrRemoveMenuItems`, e `UnloadLibraries` funções para finalizar limpando o suplemento do estado Offline. 
  
### <a name="cmyaddinhrtermaddin-example"></a>Exemplo de CMyAddin::HrTermAddin()

```cpp
HRESULT CMyAddin::HrTermAddin() 
{ 
    HRESULT hRes = S_OK; 
    DeInitMonitor(); 
    hRes =  HrRemoveMenuItems(); 
    UnloadLibraries(); 
    return hRes; 
}
```

## <a name="deinitialize-monitor-routine"></a>Deinitialize rotina de Monitor

O `inDeInitMonitor` função chama a função [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar os retornos de chamada para o objeto offline. 
  
### <a name="deinitmonitor-example"></a>Exemplo de DeInitMonitor()

```cpp
void DeInitMonitor() 
{ 
Log(true,_T("Deinitializing Outlook Offline State Monitor\n")); 
HRESULT hRes = S_OK; 
if (g_lpOfflineMgr) 
{ 
hRes = g_lpOfflineMgr->Unadvise(MAPIOFFLINE_UNADVISE_DEFAULT, g_ulAdviseToken); 
g_lpOfflineMgr->Release(); 
g_lpOfflineMgr = NULL; 
g_ulAdviseToken = NULL; 
} 
}
```

## <a name="remove-menu-items-routine"></a>Remover a rotina de itens de Menu

O `HrRemoveMenuItems` chamadas de função `DispEventUnadvise` para cada item de menu no menu **Estado Offline** e exclui o menu do **Estado Offline** . 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>Exemplo de CMyAddin::HrRemoveMenuItems()

```cpp
HRESULT CMyAddin::HrRemoveMenuItems() 
{     
    Log(true,"HrRemoveMenuItems\n"); 
    HRESULT hRes = S_OK; 
    if (m_fMenuItemsAdded) 
    { 
        try 
        { 
            if (m_spInitButton) 
            { 
                m_InitButtonHandler.DispEventUnadvise(m_spInitButton); 
            } 
            if (m_spDeinitButton) 
            { 
                m_DeinitButtonHandler.DispEventUnadvise(m_spDeinitButton); 
            } 
            if (m_spGetStateButton) 
            { 
                m_GetStateButtonHandler.DispEventUnadvise(m_spGetStateButton); 
            } 
            if (m_spSetStateButton) 
            { 
                m_SetStateButtonHandler.DispEventUnadvise(m_spSetStateButton); 
            } 
 
            m_spMyMenu->Delete(); 
        } 
        catch(_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = false; 
        } 
    } 
    return hRes; 
}
```

## <a name="unload-libraries-routine"></a>Descarregar a rotina de bibliotecas

Quando o suplemento seja descarregado do Outlook, o `UnloadLibraries` função descarrega as bibliotecas de vínculos dinâmicos (DLLs) que o suplemento necessários. 
  
### <a name="unloadlibraries-example"></a>Exemplo de UnloadLibraries()

```cpp
void UnloadLibraries() 
{ 
    Log(true,_T("UnloadLibraries - freeing modules\n")); 
    pfnHrOpenOfflineObj = NULL; 
    pfnMAPIFreeBuffer = NULL; 
    if (hModMSMAPI) FreeLibrary(hModMSMAPI); 
    hModMSMAPI = NULL; 
    if (hModMAPI) FreeLibrary(hModMAPI); 
    hModMAPI = NULL; 
    if (hModMAPIStub) FreeLibrary(hModMAPIStub); 
    hModMAPIStub = NULL; 
}
```

## <a name="see-also"></a>Confira também

- [Sobre a API de estado offline](about-the-offline-state-api.md)
- [Instalar o exemplo de suplemento de estado offline](installing-the-sample-offline-state-add-in.md)
- [Sobre o exemplo de suplemento de estado offline](about-the-sample-offline-state-add-in.md)
- [Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md)
- [Monitorar alterações de estado da conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

