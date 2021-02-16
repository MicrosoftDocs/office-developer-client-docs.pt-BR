---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348094"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="82c1e-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="82c1e-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="82c1e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82c1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82c1e-105">Força a expedição de todas as notificações na fila.</span><span class="sxs-lookup"><span data-stu-id="82c1e-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82c1e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="82c1e-106">Header file:</span></span>  <br/> |<span data-ttu-id="82c1e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="82c1e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="82c1e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="82c1e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="82c1e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="82c1e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="82c1e-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="82c1e-110">Called by:</span></span>  <br/> |<span data-ttu-id="82c1e-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="82c1e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="82c1e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82c1e-112">Parameters</span></span>

 <span data-ttu-id="82c1e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82c1e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="82c1e-114">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="82c1e-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="82c1e-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="82c1e-115">Return value</span></span>

<span data-ttu-id="82c1e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="82c1e-116">S_OK</span></span>
  
> <span data-ttu-id="82c1e-117">Todas as notificações em fila foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="82c1e-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="82c1e-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="82c1e-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="82c1e-119">WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION foi recebido.</span><span class="sxs-lookup"><span data-stu-id="82c1e-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="82c1e-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="82c1e-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="82c1e-121">O MAPI não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="82c1e-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82c1e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="82c1e-122">Remarks</span></span>

<span data-ttu-id="82c1e-123">A **função HrDispatchNotifications** faz com que o MAPI envie todas as notificações que estão atualmente na fila no mecanismo de notificação MAPI sem aguardar uma expedição de mensagem.</span><span class="sxs-lookup"><span data-stu-id="82c1e-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="82c1e-124">Isso pode ter um efeito benéfico na utilização da memória.</span><span class="sxs-lookup"><span data-stu-id="82c1e-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="82c1e-125">Para obter mais informações, consulte [Forçar uma notificação.](forcing-a-notification.md)</span><span class="sxs-lookup"><span data-stu-id="82c1e-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82c1e-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="82c1e-126">Notes to callers</span></span>

<span data-ttu-id="82c1e-127">Alguns aplicativos aguardam uma mensagem de notificação em um loop de tempo livre usando as funções Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) e [DispatchMessage.](https://msdn.microsoft.com/library/ms644934.aspx)</span><span class="sxs-lookup"><span data-stu-id="82c1e-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="82c1e-128">Em todas as plataformas, menos as mais rápidas, esses aplicativos podem experimentar um desempenho ruim ou até mesmo bloquear notificações.</span><span class="sxs-lookup"><span data-stu-id="82c1e-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="82c1e-129">Usar **HrDispatchNotifications** não só reduz o código, mas melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="82c1e-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

