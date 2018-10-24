---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579442"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="1b1d5-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="1b1d5-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="1b1d5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b1d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b1d5-105">Notifica o Visualizador de formulário que a mensagem atual tiver sido enviada para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1b1d5-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="1b1d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b1d5-106">Parameters</span></span>

<span data-ttu-id="1b1d5-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1b1d5-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1b1d5-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1b1d5-108">Return value</span></span>

<span data-ttu-id="1b1d5-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b1d5-109">S_OK</span></span> 
  
> <span data-ttu-id="1b1d5-110">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1b1d5-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b1d5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b1d5-111">Remarks</span></span>

<span data-ttu-id="1b1d5-112">Um objeto form chama o método **IMAPIViewAdviseSink::OnSubmitted** após uma chamada para [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) ter retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="1b1d5-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1b1d5-113">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="1b1d5-113">Notes to implementers</span></span>

<span data-ttu-id="1b1d5-114">Após a chamada **OnSubmitted** , você pode continuar na pressuposição de que a mensagem foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="1b1d5-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="1b1d5-115">Atualize suas janelas para refletir quaisquer alterações que tenham ocorrido.</span><span class="sxs-lookup"><span data-stu-id="1b1d5-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="1b1d5-116">Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d5-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b1d5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b1d5-117">See also</span></span>



[<span data-ttu-id="1b1d5-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1b1d5-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="1b1d5-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b1d5-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

