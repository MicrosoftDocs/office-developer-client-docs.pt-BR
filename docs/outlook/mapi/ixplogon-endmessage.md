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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357348"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="052e9-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="052e9-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="052e9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="052e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="052e9-105">Informa ao provedor de transporte que o spooler MAPI concluiu seu processamento em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="052e9-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="052e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="052e9-106">Parameters</span></span>

 <span data-ttu-id="052e9-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="052e9-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="052e9-108">no Um valor de referência específica da mensagem que foi obtido em uma chamada anterior para o método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="052e9-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="052e9-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="052e9-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="052e9-110">bota Uma bitmask de sinalizadores que indica ao spooler MAPI o que ele deve fazer com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="052e9-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="052e9-111">Se nenhum sinalizador estiver definido, a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="052e9-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="052e9-112">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="052e9-112">The following flags can be set:</span></span>
    
<span data-ttu-id="052e9-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="052e9-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="052e9-114">O provedor de transporte tem todas as informações necessárias sobre esta mensagem por enquanto.</span><span class="sxs-lookup"><span data-stu-id="052e9-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="052e9-115">Quando o provedor de transporte requer mais informações ou quando ele envia a mensagem, ele notifica o spooler MAPI chamando o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED e passando o identificador de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="052e9-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="052e9-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="052e9-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="052e9-117">O provedor de transporte não está enviando a mensagem na hora atual por razões que não são condições de erro.</span><span class="sxs-lookup"><span data-stu-id="052e9-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="052e9-118">O provedor de transporte deve ser chamado novamente mais tarde para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="052e9-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="052e9-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="052e9-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="052e9-120">O provedor de transporte precisa reiniciar a mensagem passada para ela em uma chamada de método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="052e9-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="052e9-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="052e9-121">Return value</span></span>

<span data-ttu-id="052e9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="052e9-122">S_OK</span></span> 
  
> <span data-ttu-id="052e9-123">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="052e9-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="052e9-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="052e9-124">Remarks</span></span>

<span data-ttu-id="052e9-125">O spooler MAPI chama o método **IXPLogon:: endmessage** após concluir o processamento envolvido no fornecimento de informações estendidas de entrega ou não entrega.</span><span class="sxs-lookup"><span data-stu-id="052e9-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="052e9-126">Depois que essa chamada retornar, o valor no parâmetro _ulMsgRef_ não será mais válido para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="052e9-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="052e9-127">O provedor de transporte pode reutilizar o mesmo valor em uma mensagem futura.</span><span class="sxs-lookup"><span data-stu-id="052e9-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="052e9-128">Todos os objetos que o provedor de transporte abre durante a transferência de uma mensagem devem ser liberados antes de a chamada de **endmessage** retornar, com exceção do objeto de mensagem que o spooler MAPI passa para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="052e9-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="052e9-129">O objeto Message passado pelo spooler MAPI é inválido após a chamada **endmessage** .</span><span class="sxs-lookup"><span data-stu-id="052e9-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="052e9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="052e9-130">See also</span></span>



[<span data-ttu-id="052e9-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="052e9-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="052e9-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="052e9-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="052e9-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="052e9-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="052e9-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="052e9-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

