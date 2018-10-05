---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387528"
---
# <a name="imapiformadvise"></a><span data-ttu-id="b42ce-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="b42ce-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="b42ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b42ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b42ce-105">Registra um visualizador de formulário para notificações de eventos que afetam o formulário.</span><span class="sxs-lookup"><span data-stu-id="b42ce-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b42ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b42ce-106">Parameters</span></span>

 <span data-ttu-id="b42ce-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="b42ce-107">_pAdvise_</span></span>
  
> <span data-ttu-id="b42ce-108">[in] Um ponteiro para um modo de exibição avise o objeto coletor de eventos para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b42ce-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="b42ce-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="b42ce-109">_pulConnection_</span></span>
  
> <span data-ttu-id="b42ce-110">[out] Um ponteiro para um valor diferente de zero que representa um registro de notificação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b42ce-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b42ce-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b42ce-111">Return value</span></span>

<span data-ttu-id="b42ce-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b42ce-112">S_OK</span></span> 
  
> <span data-ttu-id="b42ce-113">O registro foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b42ce-113">The registration was successful.</span></span>
    
<span data-ttu-id="b42ce-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b42ce-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="b42ce-115">O registro não foi bem-sucedida devido a memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="b42ce-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b42ce-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b42ce-116">Remarks</span></span>

<span data-ttu-id="b42ce-117">Visualizadores de formulário chame o método de **IMAPIForm::Advise** de um formulário para registrar a notificação quando ocorrem alterações ao formulário.</span><span class="sxs-lookup"><span data-stu-id="b42ce-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b42ce-118">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b42ce-118">Notes to implementers</span></span>

<span data-ttu-id="b42ce-119">O ponteiro do coletor de eventos passada no parâmetro _pAdvise_ para que você pode usá-lo para chamar o método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) apropriado quando ocorre um evento de aviso de manter uma cópia do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="b42ce-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="b42ce-120">O modo de exibição de chamada de aviso de método do coletor de [AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para reter o ponteiro até que o registro de notificação será cancelado.</span><span class="sxs-lookup"><span data-stu-id="b42ce-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="b42ce-121">Defina o conteúdo do parâmetro _pulConnection_ para um número diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b42ce-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="b42ce-122">Formulários muitas implementam um objeto auxiliar para manipular o registro e as notificações subsequentes de eventos.</span><span class="sxs-lookup"><span data-stu-id="b42ce-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="b42ce-123">Para obter mais informações sobre o processo de notificação em geral, consulte a [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b42ce-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="b42ce-124">Para obter mais informações sobre a notificação e formulários, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b42ce-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b42ce-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b42ce-125">See also</span></span>



[<span data-ttu-id="b42ce-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b42ce-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="b42ce-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b42ce-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="b42ce-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b42ce-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="b42ce-129">Notificações de eventos no MAPI</span><span class="sxs-lookup"><span data-stu-id="b42ce-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="b42ce-130">Enviar e receber notificações de formulários</span><span class="sxs-lookup"><span data-stu-id="b42ce-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

