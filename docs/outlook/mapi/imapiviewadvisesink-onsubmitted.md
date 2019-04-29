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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433980"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="788f9-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="788f9-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="788f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="788f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="788f9-105">Notifica o Visualizador de formulários que a mensagem atual foi enviada ao spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="788f9-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="788f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="788f9-106">Parameters</span></span>

<span data-ttu-id="788f9-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="788f9-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="788f9-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="788f9-108">Return value</span></span>

<span data-ttu-id="788f9-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="788f9-109">S_OK</span></span> 
  
> <span data-ttu-id="788f9-110">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="788f9-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="788f9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="788f9-111">Remarks</span></span>

<span data-ttu-id="788f9-112">Um objeto Form chama o método **IMAPIViewAdviseSink:: onenviar** após uma chamada para [IMAPIMessageSite:: SubmitMessage](imapimessagesite-submitmessage.md) foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="788f9-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="788f9-113">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="788f9-113">Notes to implementers</span></span>

<span data-ttu-id="788f9-114">Após o cancelamento de **envio** ser chamado, você pode continuar supondo que a mensagem tenha sido atualizada.</span><span class="sxs-lookup"><span data-stu-id="788f9-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="788f9-115">Atualize o Windows para refletir as alterações que ocorreram.</span><span class="sxs-lookup"><span data-stu-id="788f9-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="788f9-116">Para obter mais informações sobre notificações de formulário, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="788f9-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="788f9-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="788f9-117">See also</span></span>



[<span data-ttu-id="788f9-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="788f9-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="788f9-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="788f9-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

