---
title: Desconectar-se de um suplemento de estado offline
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766411"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="63c3f-103">Desconectar-se de um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="63c3f-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="63c3f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63c3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63c3f-105">Quando o suplemento de estado offline estiver desconectado, você deve implementar funções para encerrar e limpar o suplemento corretamente.</span><span class="sxs-lookup"><span data-stu-id="63c3f-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="63c3f-106">Para obter mais informações sobre como configurar e usar o offline estado suplemento para monitorar as alterações de estado de conexão, consulte [Add-in de configuração de backup de um estado Offline](setting-up-an-offline-state-add-in.md) e [Monitoramento Conexão estado alterações usando um suplemento do estado Offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="63c3f-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="63c3f-107">Neste tópico, esses desconexão, encerrar e funções de limpeza são demonstradas usando exemplos de código a partir do suplemento de amostra Offline estado.</span><span class="sxs-lookup"><span data-stu-id="63c3f-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="63c3f-108">O suplemento de amostra Offline estado é um suplemento de COM que adiciona um menu de **Estado Offline** para o Outlook e usa a API de estado Offline.</span><span class="sxs-lookup"><span data-stu-id="63c3f-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="63c3f-109">Através do menu de estado Offline, você pode habilitar ou desabilitar o monitoramento do estado, verifique o estado atual e alterar o estado atual.</span><span class="sxs-lookup"><span data-stu-id="63c3f-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="63c3f-110">Para obter mais informações sobre como baixar e instalar o suplemento de amostra Offline estado, consulte [Instalando o suplemento de amostra Offline estado](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="63c3f-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="63c3f-111">Para obter mais informações sobre a API de estado Offline, consulte [Sobre o Offline estado API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="63c3f-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="63c3f-112">Na rotina de desconexão</span><span class="sxs-lookup"><span data-stu-id="63c3f-112">On Disconnection Routine</span></span>

<span data-ttu-id="63c3f-113">O método **IDTExtensibility2.OnDisconnection** é chamado quando o suplemento de estado Offline seja descarregado.</span><span class="sxs-lookup"><span data-stu-id="63c3f-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="63c3f-114">Você deve implementar a limpeza do código nessa função.</span><span class="sxs-lookup"><span data-stu-id="63c3f-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="63c3f-115">No exemplo a seguir, a função de **IDTExtensibility2.OnDisconnection** chama o `HrTermAddin` função.</span><span class="sxs-lookup"><span data-stu-id="63c3f-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="63c3f-116">Exemplo de CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="63c3f-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="63c3f-117">Encerrar a função de suplemento</span><span class="sxs-lookup"><span data-stu-id="63c3f-117">Terminate Add-in Function</span></span>

<span data-ttu-id="63c3f-118">O `HrTermAddin` chamadas de função a `inDeInitMonitor`, `HrRemoveMenuItems`, e `UnloadLibraries` funções para finalizar limpando o suplemento do estado Offline.</span><span class="sxs-lookup"><span data-stu-id="63c3f-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="63c3f-119">Exemplo de CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="63c3f-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="63c3f-120">Deinitialize rotina de Monitor</span><span class="sxs-lookup"><span data-stu-id="63c3f-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="63c3f-121">O `inDeInitMonitor` função chama a função [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar os retornos de chamada para o objeto offline.</span><span class="sxs-lookup"><span data-stu-id="63c3f-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="63c3f-122">Exemplo de DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="63c3f-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="63c3f-123">Remover a rotina de itens de Menu</span><span class="sxs-lookup"><span data-stu-id="63c3f-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="63c3f-124">O `HrRemoveMenuItems` chamadas de função `DispEventUnadvise` para cada item de menu no menu **Estado Offline** e exclui o menu do **Estado Offline** .</span><span class="sxs-lookup"><span data-stu-id="63c3f-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="63c3f-125">Exemplo de CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="63c3f-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="63c3f-126">Descarregar a rotina de bibliotecas</span><span class="sxs-lookup"><span data-stu-id="63c3f-126">Unload Libraries Routine</span></span>

<span data-ttu-id="63c3f-127">Quando o suplemento seja descarregado do Outlook, o `UnloadLibraries` função descarrega as bibliotecas de vínculos dinâmicos (DLLs) que o suplemento necessários.</span><span class="sxs-lookup"><span data-stu-id="63c3f-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="63c3f-128">Exemplo de UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="63c3f-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="63c3f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="63c3f-129">See also</span></span>

- [<span data-ttu-id="63c3f-130">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="63c3f-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="63c3f-131">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="63c3f-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="63c3f-132">Sobre o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="63c3f-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="63c3f-133">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="63c3f-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="63c3f-134">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="63c3f-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

