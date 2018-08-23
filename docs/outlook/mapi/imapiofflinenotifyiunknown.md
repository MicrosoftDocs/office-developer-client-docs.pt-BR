---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568144"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="8c76f-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c76f-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="8c76f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c76f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c76f-105">Suporta o Microsoft Outlook 2010 e o Microsoft Outlook 2013 em Enviar retornos de chamada de notificação para um cliente.</span><span class="sxs-lookup"><span data-stu-id="8c76f-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c76f-106">Provided by:</span><span class="sxs-lookup"><span data-stu-id="8c76f-106">Provided by:</span></span>  <br/> |<span data-ttu-id="8c76f-107">Cliente</span><span class="sxs-lookup"><span data-stu-id="8c76f-107">Client</span></span>  <br/> |
|<span data-ttu-id="8c76f-108">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="8c76f-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8c76f-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="8c76f-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8c76f-110">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="8c76f-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8c76f-111">Notify</span><span class="sxs-lookup"><span data-stu-id="8c76f-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="8c76f-112">Envia notificações para um cliente sobre alterações no estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="8c76f-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c76f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c76f-113">Remarks</span></span>

<span data-ttu-id="8c76f-114">O cliente deve implementar essa interface e passar um ponteiro para ele como um membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="8c76f-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="8c76f-115">Subsequentemente, Outlook 2010 ou Outlook 2013 poderão usar essa interface para enviar retornos de chamada de notificação para o cliente.</span><span class="sxs-lookup"><span data-stu-id="8c76f-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c76f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c76f-116">See also</span></span>



[<span data-ttu-id="8c76f-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="8c76f-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="8c76f-118">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="8c76f-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="8c76f-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8c76f-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8c76f-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="8c76f-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

