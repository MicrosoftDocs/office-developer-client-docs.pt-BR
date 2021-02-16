---
title: Monitorar alterações de estado de conexão usando um complemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d24a6d93943883a5503b57ef223d9be777af13d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431299"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="d8eae-103">Monitorar alterações de estado de conexão usando um complemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="d8eae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8eae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8eae-105">Antes de poder usar um complemento de estado offline para monitorar alterações de estado de conexão, você deve implementar funções para configurar e inicializar o complemento.</span><span class="sxs-lookup"><span data-stu-id="d8eae-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="d8eae-106">Para obter mais informações, [consulte Configurando um complemento de estado offline.](setting-up-an-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="d8eae-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="d8eae-107">Depois de configurar o complemento de estado offline, você deve usar a **[função HrOpenOfflineObj](hropenofflineobj.md)** para obter um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="d8eae-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="d8eae-108">Usando esse objeto offline, você pode inicializar seu monitor de estado e, em seguida, obter e definir o estado atual.</span><span class="sxs-lookup"><span data-stu-id="d8eae-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="d8eae-109">Neste tópico, essas funções de monitoramento de estado são demonstradas usando exemplos de código do Exemplo de Complemento de Estado Offline.</span><span class="sxs-lookup"><span data-stu-id="d8eae-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="d8eae-110">O Exemplo de Complemento de Estado Offline é um complemento COM que adiciona um menu Estado **Offline** ao Outlook e utiliza a API de Estado Offline.</span><span class="sxs-lookup"><span data-stu-id="d8eae-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="d8eae-111">Por meio do menu **Estado Offline,** você pode habilitar ou desabilitar o monitoramento de estado, verificar o estado atual e alterar o estado atual.</span><span class="sxs-lookup"><span data-stu-id="d8eae-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="d8eae-112">Para saber mais sobre como baixar e instalar a Amostra de Suplemento de Estado Offline, confira [Instalação da Amostra de Suplemento de Estado Offline](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d8eae-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="d8eae-113">Confira mais informações sobre a API de Estado Offline em [Sobre a API de Estado Offline](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="d8eae-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="d8eae-114">Quando o suplemento de estado offline está desconectado, você precisa implementar funções para encerrar corretamente e limpar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="d8eae-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="d8eae-115">Para obter mais informações, [consulte Desconectando um complemento de estado offline.](disconnecting-an-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="d8eae-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="d8eae-116">Abrir rotina de objeto offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-116">Open Offline Object routine</span></span>

<span data-ttu-id="d8eae-117">Para que o cliente seja notificado quando ocorrer uma alteração de estado de conexão, você deve chamar a **[função HrOpenOfflineObj.](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="d8eae-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="d8eae-118">Esta função abre um objeto offline que oferece suporte **[a IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8eae-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="d8eae-119">A **função HrOpenOfflineObj** é definida no arquivo de header ConnectionState.h.</span><span class="sxs-lookup"><span data-stu-id="d8eae-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d8eae-120">A **função HrOpenOfflineObj** é declarada no arquivo de header ImportProcs.h da seguinte forma:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;` .</span><span class="sxs-lookup"><span data-stu-id="d8eae-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="d8eae-121">Exemplo de HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="d8eae-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="d8eae-122">Initialize Monitor routine</span><span class="sxs-lookup"><span data-stu-id="d8eae-122">Initialize Monitor routine</span></span>

<span data-ttu-id="d8eae-123">A `InitMonitor` função chama a função **HrOpenOfflineObj.**</span><span class="sxs-lookup"><span data-stu-id="d8eae-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="d8eae-124">A `InitMonitor` função chama **CMyOfflineNotify** para que o Outlook possa enviar notificações de retorno de chamada para o cliente e registra o retorno de chamada por meio da variável **[MAPIOFFLINE_ADVISEINFO.](mapioffline_adviseinfo.md)** `AdviseInfo`</span><span class="sxs-lookup"><span data-stu-id="d8eae-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="d8eae-125">Exemplo de InitMonitor()</span><span class="sxs-lookup"><span data-stu-id="d8eae-125">InitMonitor() example</span></span>

```cpp
void InitMonitor(LPCWSTR szProfile) 
{ 
    if (!szProfile) return; 
    Log(true,_T("Initializing Outlook Offline State Monitor\n")); 
    HRESULT hRes = S_OK; 
 
    if (g_lpOfflineMgr) 
    { 
        Log(true,_T("Already initialized\n")); 
        return; 
    } 
     
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                ULONG ulCap = NULL; 
                hRes = lpOffline->GetCapabilities(&ulCap); 
                 
                if (ulCap & MAPIOFFLINE_CAPABILITY_OFFLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_OFFLINE supported\n")); 
                if (ulCap & MAPIOFFLINE_CAPABILITY_ONLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_ONLINE supported\n")); 
                 
                if (ulCap & (MAPIOFFLINE_CAPABILITY_OFFLINE | MAPIOFFLINE_CAPABILITY_ONLINE)) 
                { 
                    CMyOfflineNotify* lpImplNotify = new CMyOfflineNotify(); 
                     
                    if (lpImplNotify) 
                    { 
                        MAPIOFFLINE_ADVISEINFO AdviseInfo = {0}; 
                        AdviseInfo.ulSize = sizeof(MAPIOFFLINE_ADVISEINFO); 
                        AdviseInfo.ulClientToken = 0;// something you want to get handed back when you get the notification 
                        AdviseInfo.CallbackType = MAPIOFFLINE_CALLBACK_TYPE_NOTIFY; 
                        AdviseInfo.pCallback = lpImplNotify; 
                        AdviseInfo.ulAdviseTypes = MAPIOFFLINE_ADVISE_TYPE_STATECHANGE; 
                        AdviseInfo.ulStateMask = MAPIOFFLINE_STATE_ALL; 
                         
                        hRes = g_lpOfflineMgr->Advise(MAPIOFFLINE_ADVISE_DEFAULT, &AdviseInfo, &g_ulAdviseToken); 
                        Log(true,"ulAdviseToken = 0x%08X\n",g_ulAdviseToken); 
                    } 
                } 
                lpOffline->Release(); 
            }                 
        } 
    } 
}
```

## <a name="get-current-state-routine"></a><span data-ttu-id="d8eae-126">Obter rotina de estado atual</span><span class="sxs-lookup"><span data-stu-id="d8eae-126">Get Current State routine</span></span>

<span data-ttu-id="d8eae-127">A  `GetCurrentState` função chama a função **HrOpenOfflineObj** e usa o objeto offline para obter o estado de conexão atual.</span><span class="sxs-lookup"><span data-stu-id="d8eae-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="d8eae-128">O estado atual é retornado na  `ulCurState` variável, que é usada na função para exibir o estado atual para o  `CButtonEventHandler::Click` usuário.</span><span class="sxs-lookup"><span data-stu-id="d8eae-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="d8eae-129">Exemplo de GetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="d8eae-129">GetCurrentState() example</span></span>

```cpp
ULONG (LPCWSTR szProfile) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Getting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
    ULONG ulCurState = NULL; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                hRes = lpOffline->GetCurrentState(&ulCurState); 
                Log(true,_T("GetCurrentState returned 0x%08X\n"),hRes); 
 
                switch(ulCurState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("Current state is 0x%0X\n"),ulCurState); 
                } 
                lpOffline->Release(); 
            } 
        } 
    } 
    return ulCurState; 
}
```

## <a name="set-current-state-routine"></a><span data-ttu-id="d8eae-130">Definir rotina de estado atual</span><span class="sxs-lookup"><span data-stu-id="d8eae-130">Set Current State routine</span></span>

<span data-ttu-id="d8eae-131">A  `SetCurrentState` função chama a função **HrOpenOfflineObj** e usa o objeto offline para definir o estado de conexão atual.</span><span class="sxs-lookup"><span data-stu-id="d8eae-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="d8eae-132">A  `CButtonEventHandler::Click` função chama a função e o novo estado é passado através da  `SetCurrentState`  `ulState` variável.</span><span class="sxs-lookup"><span data-stu-id="d8eae-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="d8eae-133">Exemplo de SetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="d8eae-133">SetCurrentState() example</span></span>

```cpp
HRESULT SetCurrentState(LPCWSTR szProfile, ULONG ulFlags, ULONG ulState) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Setting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                switch(ulFlags) 
                { 
                case MAPIOFFLINE_FLAG_BLOCK: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_BLOCK\n")); 
                    break; 
                case MAPIOFFLINE_FLAG_DEFAULT: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_DEFAULT\n")); 
                    break; 
                default: 
                    Log(true,_T("Flag used: 0x%0X\n"),ulFlags); 
                } 
                switch(ulState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("New state will be 0x%0X\n"),ulState); 
                } 
                hRes = lpOffline->SetCurrentState(ulFlags, MAPIOFFLINE_STATE_OFFLINE_MASK,ulState,NULL); 
                Log(true,_T("SetCurrentState returned 0x%08X\n"),hRes); 
                 
                lpOffline->Release(); 
            } 
        } 
    } 
    return hRes; 
}
```

## <a name="notification-routine"></a><span data-ttu-id="d8eae-134">Rotina de notificação</span><span class="sxs-lookup"><span data-stu-id="d8eae-134">Notification routine</span></span>

<span data-ttu-id="d8eae-135">A **[função IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** é usada pelo Outlook para enviar notificações a um cliente quando há alterações no estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="d8eae-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="d8eae-136">Exemplo de CMyOfflineNotify::Notify()</span><span class="sxs-lookup"><span data-stu-id="d8eae-136">CMyOfflineNotify::Notify() example</span></span>

```cpp
void CMyOfflineNotify::Notify(const MAPIOFFLINE_NOTIFY *pNotifyInfo) 
{ 
    Log(true,_T("CMyOfflineNotify::Notify\n")); 
    if    (pNotifyInfo == NULL) 
    {     
        Log(true,_T("pNotifyInfo is NULL\n")); 
    } 
    else 
    { 
        Log(true,_T("pNotifyInfo->ulSize == 0x%0X\n"),pNotifyInfo->ulSize); 
        switch(pNotifyInfo->NotifyType) 
        { 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->NotifyType == 0x%08X\n"),pNotifyInfo->NotifyType); 
        } 
        Log(true,_T("pNotifyInfo->ulClientToken == 0x%0X\n"),pNotifyInfo->ulClientToken); 
        switch(pNotifyInfo->Info.StateChange.ulMask) 
        { 
            case    MAPIOFFLINE_STATE_OFFLINE_MASK: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == MAPIOFFLINE_STATE_OFFLINE_MASK\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulMask); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateOld) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateOld); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateNew) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateNew); 
        } 
    } 
    return; 
}
```

## <a name="see-also"></a><span data-ttu-id="d8eae-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8eae-137">See also</span></span>

- [<span data-ttu-id="d8eae-138">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="d8eae-139">Instalar a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="d8eae-140">Sobre a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="d8eae-141">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="d8eae-142">Desconectando um add-in de estado offline</span><span class="sxs-lookup"><span data-stu-id="d8eae-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

