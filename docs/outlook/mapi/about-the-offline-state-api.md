---
title: Sobre a API de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410480"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="46b16-103">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="46b16-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="46b16-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46b16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46b16-105">A API de Estado Offline dá suporte a retornos de chamada indicando alterações no estado de conexão de um usuário no Microsoft Outlook 2013 e no Microsoft Outlook 2010, por exemplo, de estar online no Outlook 2013 ou no Outlook 2010 para ficar offline.</span><span class="sxs-lookup"><span data-stu-id="46b16-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="46b16-106">A API usa um objeto offline global no Outlook 2013 ou no Outlook 2010 para controlar essas alterações para um determinado perfil de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="46b16-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="46b16-107">Notificação é a única forma suportada de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="46b16-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="46b16-108">Como clientes dessa API, os provedores de email que querem ser notificados sobre essas alterações de estado de conexão fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="46b16-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="46b16-109">Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="46b16-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="46b16-110">Abra um objeto offline existente para um perfil específico usando **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="46b16-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="46b16-111">Determine se o objeto tem a capacidade de fornecer notificações online ou offline usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="46b16-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="46b16-112">Registre o objeto para notificações online ou offline usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="46b16-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="46b16-113">Os provedores de email agora podem receber notificações que o Outlook 2013 ou o Outlook 2010 envia usando **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="46b16-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="46b16-114">No desligamento, remova o registro para notificações online e offline usando **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="46b16-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="46b16-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span><span class="sxs-lookup"><span data-stu-id="46b16-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="46b16-116">O cliente deve ignorar todas as outras notificações.</span><span class="sxs-lookup"><span data-stu-id="46b16-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="46b16-117">Para obter mais informações, consulte **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="46b16-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="46b16-118">Para ver um exemplo de um cliente que usa a API de Estado Offline, consulte Sobre o Exemplo de Complemento de [Estado Offline.](about-the-sample-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="46b16-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="46b16-119">O Exemplo de Complemento de Estado Offline é um complemento COM que usa a API de Estado Offline para monitorar e alterar o estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="46b16-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="46b16-120">Essa API fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="46b16-120">This API provides the following:</span></span>
  
<span data-ttu-id="46b16-121">Definições:</span><span class="sxs-lookup"><span data-stu-id="46b16-121">Definitions:</span></span>
  
- [<span data-ttu-id="46b16-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="46b16-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="46b16-123">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="46b16-123">Data types:</span></span>
  
- <span data-ttu-id="46b16-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="46b16-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="46b16-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="46b16-127">Funções:</span><span class="sxs-lookup"><span data-stu-id="46b16-127">Functions:</span></span>
  
- <span data-ttu-id="46b16-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="46b16-129">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="46b16-129">Interfaces:</span></span>
  
- <span data-ttu-id="46b16-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="46b16-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="46b16-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="46b16-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

