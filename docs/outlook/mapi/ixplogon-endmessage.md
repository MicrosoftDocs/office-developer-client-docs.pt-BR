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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414155"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="e344f-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="e344f-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="e344f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e344f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e344f-105">Informa ao provedor de transporte que o spooler MAPI concluiu o processamento em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="e344f-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e344f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e344f-106">Parameters</span></span>

 <span data-ttu-id="e344f-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="e344f-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="e344f-108">[in] Um valor de referência específico da mensagem que foi obtido em uma chamada anterior para o [método IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e344f-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="e344f-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e344f-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="e344f-110">[out] Uma máscara de bits de sinalizadores que indica ao spooler MAPI o que ele deve fazer com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e344f-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="e344f-111">Se nenhum sinalizador estiver definido, a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="e344f-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="e344f-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e344f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="e344f-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="e344f-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="e344f-114">O provedor de transporte tem todas as informações necessárias sobre essa mensagem por enquanto.</span><span class="sxs-lookup"><span data-stu-id="e344f-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="e344f-115">Quando o provedor de transporte exige mais informações ou quando ela envia a mensagem, ele notifica o spooler MAPI chamando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED e passando o identificador de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e344f-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="e344f-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="e344f-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="e344f-117">O provedor de transporte não está enviando a mensagem no momento por motivos que não são condições de erro.</span><span class="sxs-lookup"><span data-stu-id="e344f-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="e344f-118">O provedor de transporte deve ser chamado novamente mais tarde para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e344f-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="e344f-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="e344f-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="e344f-120">O provedor de transporte precisa reiniciar a mensagem passada para ele em uma chamada de método [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e344f-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e344f-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e344f-121">Return value</span></span>

<span data-ttu-id="e344f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e344f-122">S_OK</span></span> 
  
> <span data-ttu-id="e344f-123">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="e344f-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e344f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e344f-124">Remarks</span></span>

<span data-ttu-id="e344f-125">O spooler MAPI chama o método **IXPLogon::EndMessage** depois de concluir o processamento envolvido no fornecimento de informações de entrega estendida ou não entrega.</span><span class="sxs-lookup"><span data-stu-id="e344f-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="e344f-126">Depois que essa chamada retorna, o valor no  _parâmetro ulMsgRef_ não é mais válido para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e344f-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="e344f-127">O provedor de transporte pode reutilizar o mesmo valor em uma mensagem futura.</span><span class="sxs-lookup"><span data-stu-id="e344f-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="e344f-128">Todos os objetos que o provedor de transporte abre durante a transferência de uma mensagem devem ser liberados antes que a chamada **EndMessage** retorne, com exceção do objeto de mensagem que o spooler MAPI passa para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e344f-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="e344f-129">O objeto de mensagem passado pelo spooler MAPI é inválido após a **chamada EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="e344f-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e344f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e344f-130">See also</span></span>



[<span data-ttu-id="e344f-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="e344f-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="e344f-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e344f-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="e344f-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e344f-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="e344f-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e344f-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

