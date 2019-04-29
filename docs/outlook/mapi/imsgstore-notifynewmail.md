---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a8ec06fd0401a129e08a06acdb1c18785f90d4a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431775"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="6b532-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="6b532-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="6b532-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b532-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b532-105">Informa ao repositório de mensagens que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="6b532-105">Informs the message store that a new message has arrived.</span></span> <span data-ttu-id="6b532-106">Este método é chamado apenas pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b532-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="6b532-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b532-107">Parameters</span></span>

 <span data-ttu-id="6b532-108">_lpNotification_</span><span class="sxs-lookup"><span data-stu-id="6b532-108">_lpNotification_</span></span>
  
> <span data-ttu-id="6b532-109">no Um ponteiro para uma estrutura de [notificação](notification.md) que descreve a nova notificação de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b532-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b532-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6b532-110">Return value</span></span>

<span data-ttu-id="6b532-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b532-111">S_OK</span></span> 
  
> <span data-ttu-id="6b532-112">O repositório de mensagens foi notificado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b532-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b532-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b532-113">Remarks</span></span>

<span data-ttu-id="6b532-114">O método **IMsgStore:: NotifyNewMail** é chamado pelo spooler MAPI para informar ao armazenamento de mensagens que uma mensagem está pronta para entrega.</span><span class="sxs-lookup"><span data-stu-id="6b532-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6b532-115">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="6b532-115">Notes to implementers</span></span>

<span data-ttu-id="6b532-116">Quando **NotifyNewMail** é chamado, envie uma nova notificação de email a todos os clientes registrados.</span><span class="sxs-lookup"><span data-stu-id="6b532-116">When **NotifyNewMail** is called, send a new mail notification to all registered clients.</span></span> <span data-ttu-id="6b532-117">Você pode enviar a notificação chamando [IMAPISupport:: Notify](imapisupport-notify.md), se você optar por usar os métodos do objeto support ou usando sua própria implementação.</span><span class="sxs-lookup"><span data-stu-id="6b532-117">You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation.</span></span> <span data-ttu-id="6b532-118">Um cliente registrado é um que chamou [IMsgStore:: Advise](imsgstore-advise.md) e define o parâmetro _lpEntryID_ como nulo e o parâmetro _ulEventMask_ como _fnevNewMail_.</span><span class="sxs-lookup"><span data-stu-id="6b532-118">A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="6b532-119">Não modifique ou libere a memória da estrutura de [notificação](notification.md) que descreve a notificação de novo email.</span><span class="sxs-lookup"><span data-stu-id="6b532-119">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification.</span></span> <span data-ttu-id="6b532-120">Copie a estrutura de **notificação** chamando a função do utilitário [ScCopyNotifications](sccopynotifications.md) para fazer uso das informações em seus membros.</span><span class="sxs-lookup"><span data-stu-id="6b532-120">Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b532-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b532-121">See also</span></span>



[<span data-ttu-id="6b532-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="6b532-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="6b532-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="6b532-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="6b532-124">Notifica</span><span class="sxs-lookup"><span data-stu-id="6b532-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6b532-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="6b532-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="6b532-126">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6b532-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

