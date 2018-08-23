---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582466"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="b82e3-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="b82e3-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="b82e3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b82e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b82e3-105">Informa o provedor de transporte que o MAPI spooler concluído seu processamento em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="b82e3-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b82e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b82e3-106">Parameters</span></span>

 <span data-ttu-id="b82e3-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="b82e3-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="b82e3-108">[in] Um valor de referência de mensagem específicos que foi obtido em uma chamada anterior para o método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="b82e3-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="b82e3-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b82e3-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="b82e3-110">[out] Uma bitmask dos sinalizadores que indica o MAPI spooler o que ele deve fazer com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b82e3-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="b82e3-111">Se nenhum sinalizador estiverem definidas, a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="b82e3-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="b82e3-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b82e3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b82e3-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="b82e3-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="b82e3-114">O provedor de transporte tem todas as informações necessárias sobre essa mensagem por enquanto.</span><span class="sxs-lookup"><span data-stu-id="b82e3-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="b82e3-115">Quando o provedor de transporte requer mais informações ou ele enviou a mensagem, ela notifica o MAPI spooler chamando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED e passando o identificador de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b82e3-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="b82e3-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="b82e3-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="b82e3-117">O provedor de transporte não está enviando a mensagem na hora atual por motivos que não sejam condições de erro.</span><span class="sxs-lookup"><span data-stu-id="b82e3-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="b82e3-118">O provedor de transporte deve ser chamado novamente mais tarde para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b82e3-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="b82e3-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="b82e3-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="b82e3-120">O provedor de transporte precisa reiniciar a mensagem passada em uma chamada de método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="b82e3-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b82e3-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b82e3-121">Return value</span></span>

<span data-ttu-id="b82e3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b82e3-122">S_OK</span></span> 
  
> <span data-ttu-id="b82e3-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="b82e3-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b82e3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b82e3-124">Remarks</span></span>

<span data-ttu-id="b82e3-125">O MAPI spooler chama o método de **IXPLogon::EndMessage** após ele concluir o processamento envolvidos no fornecimento de entrega estendida ou informações de não entrega.</span><span class="sxs-lookup"><span data-stu-id="b82e3-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="b82e3-126">Depois que essa chamada retorna, o valor no parâmetro _ulMsgRef_ não é válido para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="b82e3-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="b82e3-127">O provedor de transporte pode reutilizar o mesmo valor em uma mensagem de futuro.</span><span class="sxs-lookup"><span data-stu-id="b82e3-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="b82e3-128">Todos os objetos que o provedor de transporte abre durante a transferência de uma mensagem devem ser liberados antes dos retornos de chamada **EndMessage** , com exceção do objeto de mensagem que o MAPI spooler passa para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b82e3-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="b82e3-129">O objeto de mensagem passado pelo spooler MAPI é inválido após a chamada **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="b82e3-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b82e3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b82e3-130">See also</span></span>



[<span data-ttu-id="b82e3-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="b82e3-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="b82e3-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="b82e3-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="b82e3-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="b82e3-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="b82e3-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b82e3-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

