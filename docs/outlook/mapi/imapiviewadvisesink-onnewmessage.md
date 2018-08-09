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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: adf9b28e941e9ead9b83660f58701f13f35cabc7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767366"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="174f2-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="174f2-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="174f2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="174f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="174f2-105">Notifica o Visualizador de formulário que um novo ou uma mensagem existente foi carregada em um formulário.</span><span class="sxs-lookup"><span data-stu-id="174f2-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="174f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="174f2-106">Parameters</span></span>

<span data-ttu-id="174f2-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="174f2-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="174f2-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="174f2-108">Return value</span></span>

<span data-ttu-id="174f2-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="174f2-109">S_OK</span></span> 
  
> <span data-ttu-id="174f2-110">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="174f2-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="174f2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="174f2-111">Remarks</span></span>

<span data-ttu-id="174f2-112">Objetos de formulário chame o método de **IMAPIViewAdviseSink::OnNewMessage** sempre que uma mensagem é carregada em um formulário usando o método o [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="174f2-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="174f2-113">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="174f2-113">Notes to implementers</span></span>

<span data-ttu-id="174f2-114">Libere o ponteiro ativo ao objeto form porque não há mais aponta para o visualizador anteriormente era visualização da mensagem.</span><span class="sxs-lookup"><span data-stu-id="174f2-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="174f2-115">Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="174f2-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="174f2-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="174f2-116">See also</span></span>



[<span data-ttu-id="174f2-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="174f2-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="174f2-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="174f2-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="174f2-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="174f2-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="174f2-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="174f2-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

