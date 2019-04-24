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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270305"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="3a03a-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a03a-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="3a03a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a03a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a03a-105">Suporta o Microsoft Outlook 2010 e o Microsoft Outlook 2013 no envio de retornos de chamada de notificação para um cliente.</span><span class="sxs-lookup"><span data-stu-id="3a03a-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a03a-106">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="3a03a-106">Provided by:</span></span>  <br/> |<span data-ttu-id="3a03a-107">Cliente</span><span class="sxs-lookup"><span data-stu-id="3a03a-107">Client</span></span>  <br/> |
|<span data-ttu-id="3a03a-108">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="3a03a-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a03a-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="3a03a-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a03a-110">Vtable order</span><span class="sxs-lookup"><span data-stu-id="3a03a-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a03a-111">Notify</span><span class="sxs-lookup"><span data-stu-id="3a03a-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="3a03a-112">Envia notificações a um cliente sobre alterações no estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="3a03a-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a03a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a03a-113">Remarks</span></span>

<span data-ttu-id="3a03a-114">O cliente deve implementar essa interface e passar um ponteiro para ela como membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="3a03a-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="3a03a-115">Subsequentemente, o Outlook 2010 ou o Outlook 2013 poderá usar essa interface para enviar retornos de chamada de notificação ao cliente.</span><span class="sxs-lookup"><span data-stu-id="3a03a-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a03a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a03a-116">See also</span></span>



[<span data-ttu-id="3a03a-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="3a03a-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="3a03a-118">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="3a03a-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="3a03a-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3a03a-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3a03a-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="3a03a-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

