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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767292"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="435f3-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="435f3-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="435f3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="435f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="435f3-105">Gera uma leitura ou relatório nonread para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="435f3-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="435f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="435f3-106">Parameters</span></span>

 <span data-ttu-id="435f3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="435f3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="435f3-108">[in] Uma bitmask dos sinalizadores que controla como o leitura ou nonread relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="435f3-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="435f3-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="435f3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="435f3-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="435f3-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="435f3-111">É gerado um relatório de nonread.</span><span class="sxs-lookup"><span data-stu-id="435f3-111">A nonread report is generated.</span></span> <span data-ttu-id="435f3-112">Se MAPI_NON_READ não estiver definida, é gerado um relatório de leitura.</span><span class="sxs-lookup"><span data-stu-id="435f3-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="435f3-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="435f3-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="435f3-114">[in] Um ponteiro para a mensagem sobre o qual o relatório deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="435f3-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="435f3-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="435f3-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="435f3-116">[além, out] Na entrada, _lppEmptyMessage_ aponta para um ponteiro para uma mensagem vazia.</span><span class="sxs-lookup"><span data-stu-id="435f3-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="435f3-117">Na saída, _lppEmptyMessage_ aponta para um ponteiro para a mensagem de relatório.</span><span class="sxs-lookup"><span data-stu-id="435f3-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="435f3-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="435f3-118">Return value</span></span>

<span data-ttu-id="435f3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="435f3-119">S_OK</span></span> 
  
> <span data-ttu-id="435f3-120">O relatório foi gerado com êxito.</span><span class="sxs-lookup"><span data-stu-id="435f3-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="435f3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="435f3-121">Remarks</span></span>

<span data-ttu-id="435f3-122">O método **IMAPISupport::ReadReceipt** é implementado apenas para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="435f3-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="435f3-123">Provedores de armazenamento de mensagem chamarem **ReadReceipt** para instruir o MAPI para gerar uma leitura ou relatório nonread da mensagem apontado pelo parâmetro _lpReadMessage_ .</span><span class="sxs-lookup"><span data-stu-id="435f3-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="435f3-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="435f3-124">Notes to callers</span></span>

<span data-ttu-id="435f3-125">Chame **ReadReceipt** quando a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida e uma das seguintes condições for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="435f3-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="435f3-126">A mensagem foi lido.</span><span class="sxs-lookup"><span data-stu-id="435f3-126">The message has been read.</span></span>
    
- <span data-ttu-id="435f3-127">A mensagem foi movida.</span><span class="sxs-lookup"><span data-stu-id="435f3-127">The message has been moved.</span></span>
    
- <span data-ttu-id="435f3-128">A mensagem foi copiada.</span><span class="sxs-lookup"><span data-stu-id="435f3-128">The message has been copied.</span></span>
    
- <span data-ttu-id="435f3-129">Método de [IMessage::SetReadFlag](imessage-setreadflag.md) da mensagem foi chamado.</span><span class="sxs-lookup"><span data-stu-id="435f3-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="435f3-130">Não chame **ReadReceipt** quando uma mensagem é excluída.</span><span class="sxs-lookup"><span data-stu-id="435f3-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="435f3-131">Uma leitura ou relatório nonread deverão ser enviado apenas uma vez para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="435f3-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="435f3-132">Manter um registro de status de leitura da mensagem e não envie vários relatórios de uma única mensagem.</span><span class="sxs-lookup"><span data-stu-id="435f3-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="435f3-133">Se o parâmetro _lppEmptyMessage_ aponta para uma mensagem de relatório válido quando MAPI retorna da **ReadReceipt**, chame o método de [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar a mensagem e solte o ponteiro chamando seu **IUnknown:s:Release **método.</span><span class="sxs-lookup"><span data-stu-id="435f3-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="435f3-134">Se **ReadReceipt** falhar, a mensagem deve ser liberada sem ser enviada.</span><span class="sxs-lookup"><span data-stu-id="435f3-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="435f3-135">Se você armazenar status de leitura da mensagem, você pode tentar gerar o relatório nonread ou leitura mais tarde.</span><span class="sxs-lookup"><span data-stu-id="435f3-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="435f3-136">Você pode ocultar ou exibir relatórios de leitura e nonread gerados pelo repositórios em suas pastas.</span><span class="sxs-lookup"><span data-stu-id="435f3-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="435f3-137">Armazenando relatórios de leitura e nonread em pastas ocultas permite implementar maior segurança.</span><span class="sxs-lookup"><span data-stu-id="435f3-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="435f3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="435f3-138">See also</span></span>



[<span data-ttu-id="435f3-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="435f3-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="435f3-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="435f3-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="435f3-141">Propriedade canônica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="435f3-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="435f3-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="435f3-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

