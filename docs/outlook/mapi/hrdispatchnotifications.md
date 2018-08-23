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
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594695"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="a6e4a-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="a6e4a-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="a6e4a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6e4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6e4a-105">Força expedir de todas as notificações na fila.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6e4a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a6e4a-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6e4a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a6e4a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a6e4a-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a6e4a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6e4a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a6e4a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a6e4a-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a6e4a-110">Called by:</span></span>  <br/> |<span data-ttu-id="a6e4a-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a6e4a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a6e4a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6e4a-112">Parameters</span></span>

 <span data-ttu-id="a6e4a-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6e4a-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a6e4a-114">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6e4a-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a6e4a-115">Return value</span></span>

<span data-ttu-id="a6e4a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6e4a-116">S_OK</span></span>
  
> <span data-ttu-id="a6e4a-117">Tem sido despachadas todas as notificações na fila.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="a6e4a-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a6e4a-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="a6e4a-119">WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION foi recebida.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="a6e4a-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a6e4a-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="a6e4a-121">MAPI não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6e4a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6e4a-122">Remarks</span></span>

<span data-ttu-id="a6e4a-123">A função **HrDispatchNotifications** faz com que o MAPI expedir todas as notificações que estão atualmente enfileiradas no mecanismo de notificação de MAPI sem esperar por uma expedição de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="a6e4a-124">Isso pode ter um efeito vantajoso na utilização de memória.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="a6e4a-125">Para obter mais informações, consulte [forçando uma notificação](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="a6e4a-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6e4a-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a6e4a-126">Notes to callers</span></span>

<span data-ttu-id="a6e4a-127">Alguns aplicativos Aguarde uma mensagem de notificação em um loop de tempo limite usando o Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) e funções [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a6e4a-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="a6e4a-128">Em todos exceto as plataformas mais rápidas, tais aplicativos podem sofrer baixo desempenho ou bloqueio par de notificações.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="a6e4a-129">Usando **HrDispatchNotifications** não apenas reduz o código, mas melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a6e4a-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

