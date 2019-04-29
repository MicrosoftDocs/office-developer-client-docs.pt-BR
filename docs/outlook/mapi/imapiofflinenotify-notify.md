---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410690"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="95a34-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="95a34-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="95a34-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95a34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95a34-105">Envia notificações ao cliente sobre alterações no estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="95a34-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="95a34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95a34-106">Parameters</span></span>

 <span data-ttu-id="95a34-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="95a34-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="95a34-108">no A notificação que o Outlook envia ao cliente.</span><span class="sxs-lookup"><span data-stu-id="95a34-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="95a34-109">A notificação indica a parte do estado de conexão que foi alterada, o estado de conexão antigo e o estado da nova conexão.</span><span class="sxs-lookup"><span data-stu-id="95a34-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95a34-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="95a34-110">Remarks</span></span>

<span data-ttu-id="95a34-111">O Outlook usa este método para enviar retornos de chamada de notificação para um cliente.</span><span class="sxs-lookup"><span data-stu-id="95a34-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="95a34-112">Para tornar esta interface disponível para o Microsoft Outlook 2010 ou o Microsoft Outlook 2013, o cliente deve implementar essa interface e passar um ponteiro para ela como membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar os retornos de chamada usando o **[IMAPIOfflineMgr:: Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="95a34-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="95a34-113">O cliente também passa para o **MAPIOFFLINE_ADVISEINFO** um token de cliente que o Outlook 2010 ou o Outlook 2013 usa no **IMAPIOfflineNotify:: notifique** para identificar o cliente registrado para o retorno de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="95a34-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="95a34-114">Em geral, o Outlook 2010 e o Outlook 2013 podem notificar um cliente sobre alterações online/offline e outras alterações de estado de conexão, mas a API de estado offline suporta apenas notificações para alterações online/offline.</span><span class="sxs-lookup"><span data-stu-id="95a34-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="95a34-115">O cliente deve ignorar todas as outras notificações.</span><span class="sxs-lookup"><span data-stu-id="95a34-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95a34-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="95a34-116">See also</span></span>



[<span data-ttu-id="95a34-117">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="95a34-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="95a34-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="95a34-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

