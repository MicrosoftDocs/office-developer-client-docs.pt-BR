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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427723"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="c60eb-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c60eb-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="c60eb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c60eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c60eb-105">Cria um coletor de aviso que quebra um coletor de aviso existente para segurança de thread.</span><span class="sxs-lookup"><span data-stu-id="c60eb-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c60eb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c60eb-106">Header file:</span></span>  <br/> |<span data-ttu-id="c60eb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="c60eb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c60eb-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c60eb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c60eb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c60eb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c60eb-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c60eb-110">Called by:</span></span>  <br/> |<span data-ttu-id="c60eb-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c60eb-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="c60eb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c60eb-112">Parameters</span></span>

 <span data-ttu-id="c60eb-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c60eb-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c60eb-114">no Ponteiro para o coletor de aviso a ser quebrado.</span><span class="sxs-lookup"><span data-stu-id="c60eb-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="c60eb-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c60eb-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="c60eb-116">bota Ponteiro para um ponteiro para um novo coletor de aviso que envolve o coletor de avisos apontado pelo parâmetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="c60eb-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c60eb-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c60eb-117">Return value</span></span>

<span data-ttu-id="c60eb-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c60eb-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c60eb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c60eb-119">Remarks</span></span>

<span data-ttu-id="c60eb-120">O objetivo do wrapper é certificar-se de que a notificação é chamada no mesmo thread que chamou a função **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="c60eb-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="c60eb-121">Essa função é usada para proteger os retornos de chamada de notificação que devem ser executados em um thread específico.</span><span class="sxs-lookup"><span data-stu-id="c60eb-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="c60eb-122">Os aplicativos cliente devem usar **HrThisThreadAdviseSink** para restringir quando as notificações são geradas, ou seja, quando as chamadas são feitas para o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do objeto de coletor de aviso passado pelo cliente em um \*\*aviso anterior \*\*chamada.</span><span class="sxs-lookup"><span data-stu-id="c60eb-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="c60eb-123">Se as notificações tiverem permissão para serem geradas arbitrariamente, uma implementação de notificação poderá forçar um cliente a executar uma operação multithread quando não for apropriado.</span><span class="sxs-lookup"><span data-stu-id="c60eb-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="c60eb-124">Por exemplo, um cliente pode usar uma biblioteca, como uma das bibliotecas de classe Microsoft Foundation, que não oferece suporte a chamadas multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="c60eb-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="c60eb-125">A notificação em um thread diferente faria com que um cliente fosse difícil de testar e propenso a erros.</span><span class="sxs-lookup"><span data-stu-id="c60eb-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="c60eb-126">O **HrThisThreadAdviseSink** garante que as chamadas OnNotify ocorram somente nos seguintes horários apropriados: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c60eb-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="c60eb-127">Durante o processamento de uma chamada para qualquer método MAPI.</span><span class="sxs-lookup"><span data-stu-id="c60eb-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="c60eb-128">Durante o processamento de mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="c60eb-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="c60eb-129">Quando o **HrThisThreadAdviseSink** é implementado, todas as chamadas para o novo método **OnNotify** do coletor de avisos em qualquer thread fazem com que o método de notificação original seja executado no thread no qual o **HrThisThreadAdviseSink** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="c60eb-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="c60eb-130">Para obter mais informações sobre notificações e coletores de aviso, consulte [Event Notification in MAPI](event-notification-in-mapi.md) e [implementar um objeto de coletor de aviso](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="c60eb-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

