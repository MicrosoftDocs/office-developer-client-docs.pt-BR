---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766836"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="dd0b0-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dd0b0-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="dd0b0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd0b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd0b0-105">Cria um coletor de advise que dispõe de um coletor advise existente para a segurança do thread.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd0b0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dd0b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd0b0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dd0b0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dd0b0-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="dd0b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd0b0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd0b0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd0b0-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="dd0b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd0b0-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="dd0b0-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="dd0b0-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="dd0b0-112">Parameters</span></span>

 <span data-ttu-id="dd0b0-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="dd0b0-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="dd0b0-114">[in] Ponteiro para o coletor de eventos advise para ser quebradas.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="dd0b0-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="dd0b0-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="dd0b0-116">[out] Ponteiro para um ponteiro para um novo coletor de advise que envolve o coletor de eventos advise apontado pelo parâmetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="dd0b0-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dd0b0-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dd0b0-117">Return value</span></span>

<span data-ttu-id="dd0b0-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd0b0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd0b0-119">Remarks</span></span>

<span data-ttu-id="dd0b0-120">A finalidade do wrapper é certificar-se de que a notificação é chamada no mesmo thread que a chamada de função **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="dd0b0-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="dd0b0-121">Essa função é usada para proteger os retornos de chamada de notificação que devem ser executado em um determinado segmento.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="dd0b0-122">Aplicativos cliente devem usar **HrThisThreadAdviseSink** para restringir quando as notificações são geradas, ou seja, quando chamadas forem feitas para o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do objeto coletor advise passado pelo cliente em uma **anterior Advise **chamada.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="dd0b0-123">Se as notificações são permitidas a serem gerados arbitrariamente uma implementação de notificação pode forçar um cliente em operação multithreaded quando que não ser apropriada.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="dd0b0-124">Por exemplo, um cliente pode usar uma biblioteca, como um das bibliotecas de classes do Microsoft Foundation, que não oferece suporte a chamadas multithread.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="dd0b0-125">Notificação em um segmento diferente tornaria tal um cliente difícil testar e propenso a erros.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="dd0b0-126">**HrThisThreadAdviseSink** certifica-se de que as chamadas **OnNotify** ocorrem apenas nesses momentos apropriado:</span><span class="sxs-lookup"><span data-stu-id="dd0b0-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="dd0b0-127">Durante o processamento de uma chamada para qualquer método MAPI.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="dd0b0-128">Durante o processamento de mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="dd0b0-129">Quando **HrThisThreadAdviseSink** é implementado, quaisquer chamadas ao método de **OnNotify** do coletor de advise novo em qualquer segmento fazer com que o método de notificação original a ser executado no thread no qual **HrThisThreadAdviseSink** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="dd0b0-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="dd0b0-130">Para obter mais informações sobre a notificação e receptores de aviso, consulte a [Notificação de evento em MAPI](event-notification-in-mapi.md) e a [implementação de um objeto coletor de aviso](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="dd0b0-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

