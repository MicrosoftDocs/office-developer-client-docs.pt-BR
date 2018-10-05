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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385561"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="9e15b-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="9e15b-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="9e15b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e15b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e15b-105">Força expedir de todas as notificações na fila.</span><span class="sxs-lookup"><span data-stu-id="9e15b-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e15b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9e15b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e15b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9e15b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9e15b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9e15b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e15b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9e15b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9e15b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9e15b-110">Called by:</span></span>  <br/> |<span data-ttu-id="9e15b-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="9e15b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9e15b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e15b-112">Parameters</span></span>

 <span data-ttu-id="9e15b-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e15b-113">_ulFlags_</span></span>
  
> <span data-ttu-id="9e15b-114">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9e15b-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9e15b-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9e15b-115">Return value</span></span>

<span data-ttu-id="9e15b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e15b-116">S_OK</span></span>
  
> <span data-ttu-id="9e15b-117">Tem sido despachadas todas as notificações na fila.</span><span class="sxs-lookup"><span data-stu-id="9e15b-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="9e15b-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9e15b-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="9e15b-119">WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION foi recebida.</span><span class="sxs-lookup"><span data-stu-id="9e15b-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="9e15b-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9e15b-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="9e15b-121">MAPI não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="9e15b-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e15b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e15b-122">Remarks</span></span>

<span data-ttu-id="9e15b-123">A função **HrDispatchNotifications** faz com que o MAPI expedir todas as notificações que estão atualmente enfileiradas no mecanismo de notificação de MAPI sem esperar por uma expedição de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9e15b-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="9e15b-124">Isso pode ter um efeito vantajoso na utilização de memória.</span><span class="sxs-lookup"><span data-stu-id="9e15b-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="9e15b-125">Para obter mais informações, consulte [forçando uma notificação](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="9e15b-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e15b-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9e15b-126">Notes to callers</span></span>

<span data-ttu-id="9e15b-127">Alguns aplicativos Aguarde uma mensagem de notificação em um loop de tempo limite usando o Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) e funções [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9e15b-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="9e15b-128">Em todos exceto as plataformas mais rápidas, tais aplicativos podem sofrer baixo desempenho ou bloqueio par de notificações.</span><span class="sxs-lookup"><span data-stu-id="9e15b-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="9e15b-129">Usando **HrDispatchNotifications** não apenas reduz o código, mas melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="9e15b-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

