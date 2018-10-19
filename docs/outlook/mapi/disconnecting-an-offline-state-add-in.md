---
title: Desconectar-se de um suplemento de estado offline
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Última modificação: 07 de dezembro de 2015'
ms.openlocfilehash: ce25c6777c8a71da0fe11e0bbf34eefafe2ca50d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564133"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Desconectar-se de um suplemento de estado offline

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando o suplemento de estado offline está desconectado, você precisa implementar funções para encerrar corretamente e limpar o suplemento. Para saber mais sobre como configurar e usar o suplemento de estado offline para monitorar as alterações de estado da conexão, confira [Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md) e [Monitorar alterações de estado de conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
Neste tópico, essas funções de desconexão, encerramento e limpeza são demonstradas pelo uso de exemplos de código da Amostra de Suplemento de Estado Offline. O suplemento do estado de Offline de amostra é um suplemento COM que adiciona uma **estado Offline** menu ao Outlook e usa a API de estado Offline. Pelo menu Estado Offline, você pode habilitar ou desabilitar o monitoramento do estado e verificar e alterar o estado atual. Para saber mais sobre como baixar e instalar a Amostra de Suplemento de Estado Offline, confira [Instalação da Amostra de Suplemento de Estado Offline](installing-the-sample-offline-state-add-in.md). Confira mais informações sobre a API de Estado Offline em [Sobre a API de Estado Offline](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Sobre a Rotina de Desconexão

O método **IDTExtensibility2.OnDisconnection** é chamado quando o suplemento de estado offline é descarregado. Você deve implementar um código de limpeza nesta função. No exemplo a seguir, a função **IDTExtensibility2.OnDisconnection** chama a função `HrTermAddin`. 
  
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

A função `HrTermAddin` chama as funções `inDeInitMonitor`, `HrRemoveMenuItems` e `UnloadLibraries` para terminar a limpeza do suplemento de estado offline. 
  
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

## <a name="deinitialize-monitor-routine"></a>Desinicializar rotina de monitor

A função `inDeInitMonitor` chama a função [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar os retornos de chamada do objeto offline. 
  
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

## <a name="remove-menu-items-routine"></a>Remover rotina de itens do menu

A função `HrRemoveMenuItems` chama `DispEventUnadvise` para cada item do menu do menu **Estado Offline**, e depois exclui o menu **Estado Offline**. 
  
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

## <a name="unload-libraries-routine"></a>Descarregar rotinas de bibliotecas

Quando o suplemento for descarregado do Outlook, a função `UnloadLibraries` descarrega as bibliotecas de vínculo dinâmico (DLLs) que o suplemento exigiu. 
  
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
- [Instalar a amostra de suplemento de estado offline](installing-the-sample-offline-state-add-in.md)
- [Sobre a amostra de suplemento de estado offline](about-the-sample-offline-state-add-in.md)
- [Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md)
- [Monitorar alterações de estado da conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

