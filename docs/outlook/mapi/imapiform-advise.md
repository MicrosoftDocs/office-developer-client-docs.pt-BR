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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329481"
---
# <a name="imapiformadvise"></a><span data-ttu-id="32524-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="32524-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="32524-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32524-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32524-105">Registra um visualizador de formulários para notificações sobre eventos que afetam o formulário.</span><span class="sxs-lookup"><span data-stu-id="32524-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="32524-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32524-106">Parameters</span></span>

 <span data-ttu-id="32524-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="32524-107">_pAdvise_</span></span>
  
> <span data-ttu-id="32524-108">no Um ponteiro para um objeto de coletor de aviso de exibição para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="32524-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="32524-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="32524-109">_pulConnection_</span></span>
  
> <span data-ttu-id="32524-110">bota Um ponteiro para um valor diferente de zero que representa um registro de notificação bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="32524-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32524-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="32524-111">Return value</span></span>

<span data-ttu-id="32524-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="32524-112">S_OK</span></span> 
  
> <span data-ttu-id="32524-113">O registro foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="32524-113">The registration was successful.</span></span>
    
<span data-ttu-id="32524-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="32524-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="32524-115">O registro não foi bem-sucedido devido à memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="32524-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32524-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="32524-116">Remarks</span></span>

<span data-ttu-id="32524-117">Os visualizadores de formulários chamam o método **IMAPIForm:: Advise** de um formulário para registrar a notificação quando ocorrerem alterações no formulário.</span><span class="sxs-lookup"><span data-stu-id="32524-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="32524-118">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="32524-118">Notes to implementers</span></span>

<span data-ttu-id="32524-119">Mantenha uma cópia do ponteiro View Advise Sink passado no parâmetro _pAdvise_ para que você possa usá-lo para chamar o método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) apropriado quando ocorre um evento.</span><span class="sxs-lookup"><span data-stu-id="32524-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="32524-120">Chame o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do coletor de avisos de exibição para manter o ponteiro até que o registro de notificação seja cancelado.</span><span class="sxs-lookup"><span data-stu-id="32524-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="32524-121">Defina o conteúdo do parâmetro _pulConnection_ para um número diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="32524-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="32524-122">Muitos formulários implementam um objeto auxiliar para lidar com o registro e a notificação subsequente de eventos.</span><span class="sxs-lookup"><span data-stu-id="32524-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="32524-123">Para obter mais informações sobre o processo de notificação em geral, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="32524-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="32524-124">Para obter mais informações sobre notificações e formulários, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="32524-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32524-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="32524-125">See also</span></span>



[<span data-ttu-id="32524-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="32524-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="32524-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32524-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="32524-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32524-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="32524-129">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="32524-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="32524-130">Enviar e receber notificações de formulário</span><span class="sxs-lookup"><span data-stu-id="32524-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

