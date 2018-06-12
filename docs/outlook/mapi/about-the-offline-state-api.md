---
title: Sobre a API de estado Offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766115"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="63f75-103">Sobre a API de estado Offline</span><span class="sxs-lookup"><span data-stu-id="63f75-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="63f75-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63f75-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63f75-105">A API de estado Offline oferece suporte a chamadas de retorno indicando alterações no estado de conexão de um usuário no Microsoft Outlook 2013 e o Microsoft Outlook 2010 — por exemplo, de sendo online no Outlook 2013 ou o Outlook 2010 para sendo offline.</span><span class="sxs-lookup"><span data-stu-id="63f75-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="63f75-106">A API usa um objeto global de offline no Outlook 2013 ou o Outlook 2010 para rastrear tais alterações para um perfil de conta de usuário específico.</span><span class="sxs-lookup"><span data-stu-id="63f75-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="63f75-107">Notificação é a única forma com suporte de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="63f75-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="63f75-108">Como os clientes desta API, provedores de email que desejam ser notificado sobre essas alterações de estado de conexão faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="63f75-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="63f75-109">Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="63f75-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="63f75-110">Abra um objeto offline existente para um perfil específico usando **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="63f75-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="63f75-111">Determine se o objeto tem a capacidade de fornecer notificações online ou offline, usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="63f75-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="63f75-112">Registre o objeto para notificações online ou offline, usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="63f75-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="63f75-113">Provedores de email agora podem receber notificações que Outlook 2013 ou o Outlook 2010 envia usando **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="63f75-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="63f75-114">No desligamento, remova o registro para notificações online e offline usando **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="63f75-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="63f75-115">Em geral, o Outlook 2013 e o Outlook 2010 podem notificá-um cliente de alterações online offline, bem como outras alterações, mas a API de estado Offline dá suporte a notificações apenas para alterações online offline.</span><span class="sxs-lookup"><span data-stu-id="63f75-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="63f75-116">O cliente deve ignorar todos os outras notificações.</span><span class="sxs-lookup"><span data-stu-id="63f75-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="63f75-117">Para obter mais informações, consulte **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** e **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="63f75-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="63f75-118">Para obter um exemplo de um cliente que usa a API de estado Offline, consulte [sobre a amostra Offline estado Add-in](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="63f75-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="63f75-119">O suplemento de amostra Offline estado é um suplemento de COM que usa a API de estado Offline para monitorar e alterar o estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="63f75-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="63f75-120">Essa API oferece os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="63f75-120">This API provides the following:</span></span>
  
<span data-ttu-id="63f75-121">Definições:</span><span class="sxs-lookup"><span data-stu-id="63f75-121">Definitions:</span></span>
  
- [<span data-ttu-id="63f75-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="63f75-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="63f75-123">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="63f75-123">Data types:</span></span>
  
- <span data-ttu-id="63f75-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="63f75-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="63f75-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="63f75-127">Funções:</span><span class="sxs-lookup"><span data-stu-id="63f75-127">Functions:</span></span>
  
- <span data-ttu-id="63f75-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="63f75-129">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="63f75-129">Interfaces:</span></span>
  
- <span data-ttu-id="63f75-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="63f75-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="63f75-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="63f75-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

