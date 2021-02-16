---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419601"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="47e81-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="47e81-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="47e81-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47e81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47e81-105">Notifica o visualizador de formulário de que uma mensagem nova ou existente foi carregada em um formulário.</span><span class="sxs-lookup"><span data-stu-id="47e81-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="47e81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47e81-106">Parameters</span></span>

<span data-ttu-id="47e81-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="47e81-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="47e81-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="47e81-108">Return value</span></span>

<span data-ttu-id="47e81-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="47e81-109">S_OK</span></span> 
  
> <span data-ttu-id="47e81-110">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47e81-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47e81-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="47e81-111">Remarks</span></span>

<span data-ttu-id="47e81-112">Objetos de formulário chamam o método **IMAPIViewAdviseSink::OnNewMessage** sempre que uma mensagem é carregada em um formulário usando o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load.](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="47e81-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="47e81-113">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="47e81-113">Notes to implementers</span></span>

<span data-ttu-id="47e81-114">Libere seu ponteiro ativo para o objeto de formulário porque ele não aponta mais para a mensagem que seu visualizador estava visualizando anteriormente.</span><span class="sxs-lookup"><span data-stu-id="47e81-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="47e81-115">Para obter mais informações sobre notificações de formulário, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="47e81-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47e81-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="47e81-116">See also</span></span>



[<span data-ttu-id="47e81-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47e81-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="47e81-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="47e81-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="47e81-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="47e81-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="47e81-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47e81-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

