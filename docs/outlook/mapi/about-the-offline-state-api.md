---
title: Sobre a API de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321781"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="6254e-103">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="6254e-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="6254e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6254e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6254e-105">A API de estado offline oferece suporte a retornos de chamada que indicam alterações no estado de conexão de um usuário no Microsoft Outlook 2013 e no Microsoft Outlook 2010 — por exemplo, de ser online no Outlook 2013 ou no Outlook 2010 para ser offline.</span><span class="sxs-lookup"><span data-stu-id="6254e-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="6254e-106">A API usa um objeto offline global no Outlook 2013 ou no Outlook 2010 para controlar essas alterações para um determinado perfil de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="6254e-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="6254e-107">A notificação é a única forma de retorno de chamada com suporte.</span><span class="sxs-lookup"><span data-stu-id="6254e-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="6254e-108">Como clientes desta API, os provedores de email que desejam ser notificados dessas alterações de estado de conexão fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6254e-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="6254e-109">Implementar o **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="6254e-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="6254e-110">Abra um objeto offline existente para um perfil específico usando **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="6254e-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="6254e-111">Determinar se o objeto tem a capacidade de fornecer notificações online ou offline usando o **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="6254e-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="6254e-112">Registre o objeto para notificações online ou offline usando o **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="6254e-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="6254e-113">Os provedores de email agora podem receber notificações que o Outlook 2013 ou o Outlook 2010 enviar usando o **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="6254e-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="6254e-114">Ao desligar, remova o registro de notificações online e offline usando **[IMAPIOfflineMgr:: Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="6254e-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6254e-115">Em geral, o Outlook 2013 e o Outlook 2010 podem notificar um cliente sobre alterações online/offline, bem como outras alterações, mas a API de estado offline oferece suporte somente a notificações para alterações online/offline.</span><span class="sxs-lookup"><span data-stu-id="6254e-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="6254e-116">O cliente deve ignorar todas as outras notificações.</span><span class="sxs-lookup"><span data-stu-id="6254e-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="6254e-117">Para obter mais informações, consulte **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="6254e-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="6254e-118">Para obter um exemplo de um cliente que usa a API de estado offline, consulte [sobre o exemplo de suplemento de estado offline](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="6254e-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="6254e-119">O exemplo de suplemento de estado offline é um suplemento COM que usa a API de estado offline para monitorar e alterar o estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="6254e-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="6254e-120">Essa API fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6254e-120">This API provides the following:</span></span>
  
<span data-ttu-id="6254e-121">Definições:</span><span class="sxs-lookup"><span data-stu-id="6254e-121">Definitions:</span></span>
  
- [<span data-ttu-id="6254e-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6254e-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="6254e-123">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="6254e-123">Data types:</span></span>
  
- <span data-ttu-id="6254e-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="6254e-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="6254e-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="6254e-127">Funções:</span><span class="sxs-lookup"><span data-stu-id="6254e-127">Functions:</span></span>
  
- <span data-ttu-id="6254e-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="6254e-129">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="6254e-129">Interfaces:</span></span>
  
- <span data-ttu-id="6254e-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="6254e-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="6254e-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="6254e-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

