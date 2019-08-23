---
title: Desconectar-se de um suplemento de estado offline
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Última modificação: 07 de dezembro de 2015'
ms.openlocfilehash: c665bae57a72428df7acd92e080f7c31b131253b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316650"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="1c2c7-103">Desconectar-se de um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="1c2c7-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="1c2c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c2c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c2c7-105">Quando o suplemento de estado offline está desconectado, você precisa implementar funções para encerrar corretamente e limpar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="1c2c7-106">Para saber mais sobre como configurar e usar o suplemento de estado offline para monitorar as alterações de estado da conexão, confira [Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md) e [Monitorar alterações de estado de conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="1c2c7-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="1c2c7-107">Neste tópico, essas funções de desconexão, encerramento e limpeza são demonstradas pelo uso de exemplos de código da Amostra de Suplemento de Estado Offline.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="1c2c7-108">O suplemento do estado de Offline de amostra é um suplemento COM que adiciona uma **estado Offline** menu ao Outlook e usa a API de estado Offline.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="1c2c7-109">Pelo menu Estado Offline, você pode habilitar ou desabilitar o monitoramento do estado e verificar e alterar o estado atual.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="1c2c7-110">Para saber mais sobre como baixar e instalar a Amostra de Suplemento de Estado Offline, confira [Instalação da Amostra de Suplemento de Estado Offline](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="1c2c7-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="1c2c7-111">Confira mais informações sobre a API de Estado Offline em [Sobre a API de Estado Offline](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="1c2c7-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="1c2c7-112">Sobre a Rotina de Desconexão</span><span class="sxs-lookup"><span data-stu-id="1c2c7-112">On Disconnection Routine</span></span>

<span data-ttu-id="1c2c7-113">O método **IDTExtensibility2.OnDisconnection** é chamado quando o suplemento de estado offline é descarregado.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="1c2c7-114">Você deve implementar um código de limpeza nesta função.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="1c2c7-115">No exemplo a seguir, a função **IDTExtensibility2.OnDisconnection** chama a função `HrTermAddin`.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="1c2c7-116">Exemplo de CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="1c2c7-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="1c2c7-117">Encerrar a função de suplemento</span><span class="sxs-lookup"><span data-stu-id="1c2c7-117">Terminate Add-in Function</span></span>

<span data-ttu-id="1c2c7-118">A função `HrTermAddin` chama as funções `inDeInitMonitor`, `HrRemoveMenuItems` e `UnloadLibraries` para terminar a limpeza do suplemento de estado offline.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="1c2c7-119">Exemplo de CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="1c2c7-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="1c2c7-120">Desinicializar rotina de monitor</span><span class="sxs-lookup"><span data-stu-id="1c2c7-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="1c2c7-121">A função `inDeInitMonitor` chama a função [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar os retornos de chamada do objeto offline.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="1c2c7-122">Exemplo de DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="1c2c7-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="1c2c7-123">Remover rotina de itens do menu</span><span class="sxs-lookup"><span data-stu-id="1c2c7-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="1c2c7-124">A função `HrRemoveMenuItems` chama `DispEventUnadvise` para cada item do menu do menu **Estado Offline**, e depois exclui o menu **Estado Offline**.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="1c2c7-125">Exemplo de CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="1c2c7-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="1c2c7-126">Descarregar rotinas de bibliotecas</span><span class="sxs-lookup"><span data-stu-id="1c2c7-126">Unload Libraries Routine</span></span>

<span data-ttu-id="1c2c7-127">Quando o suplemento for descarregado do Outlook, a função `UnloadLibraries` descarrega as bibliotecas de vínculo dinâmico (DLLs) que o suplemento exigiu.</span><span class="sxs-lookup"><span data-stu-id="1c2c7-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="1c2c7-128">Exemplo de UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="1c2c7-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1c2c7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c2c7-129">See also</span></span>

- [<span data-ttu-id="1c2c7-130">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="1c2c7-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="1c2c7-131">Instalar a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="1c2c7-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="1c2c7-132">Sobre a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="1c2c7-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="1c2c7-133">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="1c2c7-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="1c2c7-134">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="1c2c7-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

