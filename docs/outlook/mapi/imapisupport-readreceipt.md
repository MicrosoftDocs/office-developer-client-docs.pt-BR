---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425320"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="9f9f9-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="9f9f9-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="9f9f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f9f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f9f9-105">Gera um relatório lido ou não lido para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="9f9f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f9f9-106">Parameters</span></span>

 <span data-ttu-id="9f9f9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f9f9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9f9f9-108">[in] Uma máscara de bits de sinalizadores que controla como o relatório lido ou não lido é gerado.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="9f9f9-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9f9f9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9f9f9-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="9f9f9-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="9f9f9-111">Um relatório não lido é gerado.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-111">A nonread report is generated.</span></span> <span data-ttu-id="9f9f9-112">Se MAPI_NON_READ não estiver definido, será gerado um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="9f9f9-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="9f9f9-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="9f9f9-114">[in] Um ponteiro para a mensagem sobre a qual o relatório deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="9f9f9-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="9f9f9-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="9f9f9-116">[in, out] Na entrada,  _lppEmptyMessage_ aponta para um ponteiro para uma mensagem vazia.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="9f9f9-117">Na saída,  _lppEmptyMessage_ aponta para um ponteiro para a mensagem de relatório.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9f9f9-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f9f9-118">Return value</span></span>

<span data-ttu-id="9f9f9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f9f9-119">S_OK</span></span> 
  
> <span data-ttu-id="9f9f9-120">O relatório foi gerado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f9f9-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f9f9-121">Remarks</span></span>

<span data-ttu-id="9f9f9-122">O **método IMAPISupport::ReadReceipt** é implementado somente para objetos de suporte do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="9f9f9-123">Os provedores de armazenamento de mensagens chamam **ReadReceipt** para instruir o MAPI a gerar um relatório lido ou não lido para a mensagem apontada pelo _parâmetro lpReadMessage._</span><span class="sxs-lookup"><span data-stu-id="9f9f9-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9f9f9-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9f9f9-124">Notes to callers</span></span>

<span data-ttu-id="9f9f9-125">Chame **ReadReceipt** quando a **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida e uma das seguintes condições for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="9f9f9-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="9f9f9-126">A mensagem foi lida.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-126">The message has been read.</span></span>
    
- <span data-ttu-id="9f9f9-127">A mensagem foi movida.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-127">The message has been moved.</span></span>
    
- <span data-ttu-id="9f9f9-128">A mensagem foi copiada.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-128">The message has been copied.</span></span>
    
- <span data-ttu-id="9f9f9-129">O método [IMessage::SetReadFlag](imessage-setreadflag.md) da mensagem foi chamado.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="9f9f9-130">Não chame **ReadReceipt** quando uma mensagem for excluída.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="9f9f9-131">Um relatório lido ou não lido deve ser enviado apenas uma vez para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="9f9f9-132">Acompanhe o status de leitura de uma mensagem e não envie vários relatórios para uma única mensagem.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="9f9f9-133">Se o parâmetro _lppEmptyMessage_ aponta para uma mensagem de relatório válida quando MAPI retorna de **ReadReceipt**, chame o método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar a mensagem e liberar o ponteiro chamando seu método **IUnknown:s:Release.**</span><span class="sxs-lookup"><span data-stu-id="9f9f9-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="9f9f9-134">Se **ReadReceipt** falhar, a mensagem deverá ser liberada sem ser enviada.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="9f9f9-135">Se você armazenar o status de leitura da mensagem, poderá tentar gerar o relatório lido ou não lido posteriormente.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="9f9f9-136">Você pode ocultar ou exibir relatórios lidos e não lidos gerados por armazenamentos em suas pastas.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="9f9f9-137">Armazenar relatórios lidos e não lidos em pastas ocultas permite implementar uma segurança mais rígida.</span><span class="sxs-lookup"><span data-stu-id="9f9f9-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f9f9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f9f9-138">See also</span></span>



[<span data-ttu-id="9f9f9-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="9f9f9-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="9f9f9-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9f9f9-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="9f9f9-141">Propriedade canônica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="9f9f9-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="9f9f9-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f9f9-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

