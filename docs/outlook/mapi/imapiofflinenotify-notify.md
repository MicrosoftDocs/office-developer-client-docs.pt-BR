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
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767136"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="a833f-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="a833f-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="a833f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a833f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a833f-105">Envia notificações para o cliente sobre alterações no estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="a833f-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="a833f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="a833f-106">Parameters</span></span>

 <span data-ttu-id="a833f-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="a833f-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="a833f-108">[in] A notificação informando que o Outlook enviará ao cliente.</span><span class="sxs-lookup"><span data-stu-id="a833f-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="a833f-109">A notificação indica a parte do estado de conexão que foi alterada, o estado de conexão antigo e o novo estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="a833f-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a833f-110">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a833f-110">Remarks</span></span>

<span data-ttu-id="a833f-111">O Outlook usa este método para enviar retornos de chamada de notificação para um cliente.</span><span class="sxs-lookup"><span data-stu-id="a833f-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="a833f-112">Para disponibilizar essa interface para Microsoft Outlook 2010 ou o Microsoft Outlook 2013, o cliente deve implementar essa interface e passar um ponteiro para ele como um membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="a833f-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="a833f-113">O cliente também passa para **MAPIOFFLINE_ADVISEINFO** um token de cliente que o Outlook 2010 ou Outlook 2013 usa **IMAPIOfflineNotify::Notify** para identificar o cliente registrado para o retorno de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="a833f-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="a833f-114">Em geral, o Outlook 2010 e o Outlook 2013 podem notificá-um cliente de alterações online offline e outras alterações de estado de conexão, mas a API de estado Offline dá suporte a notificações apenas para alterações online offline.</span><span class="sxs-lookup"><span data-stu-id="a833f-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="a833f-115">O cliente deve ignorar todos os outras notificações.</span><span class="sxs-lookup"><span data-stu-id="a833f-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a833f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a833f-116">See also</span></span>



[<span data-ttu-id="a833f-117">Sobre a API de estado Offline</span><span class="sxs-lookup"><span data-stu-id="a833f-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="a833f-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="a833f-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

