---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425733"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="688f0-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="688f0-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="688f0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="688f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="688f0-105">Prepara uma mensagem para envio ao spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="688f0-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="688f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="688f0-106">Parameters</span></span>

 <span data-ttu-id="688f0-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="688f0-107">_lpMessage_</span></span>
  
> <span data-ttu-id="688f0-108">[in] Um ponteiro para a mensagem a ser preparada.</span><span class="sxs-lookup"><span data-stu-id="688f0-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="688f0-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="688f0-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="688f0-110">[in, out] Na entrada, o  _parâmetro lpulFlags_ é reservado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="688f0-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="688f0-111">Na saída,  _lpulFlags_ deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="688f0-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="688f0-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="688f0-112">Return value</span></span>

<span data-ttu-id="688f0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="688f0-113">S_OK</span></span> 
  
> <span data-ttu-id="688f0-114">A mensagem foi preparada com êxito.</span><span class="sxs-lookup"><span data-stu-id="688f0-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="688f0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="688f0-115">Remarks</span></span>

<span data-ttu-id="688f0-116">O **método IMAPISupport::P repareSubmit** é implementado para objetos de suporte do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="688f0-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="688f0-117">Os provedores de armazenamento de mensagens chamam **PrepareSubmit** na implementação do método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar uma mensagem para envio ao spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="688f0-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="688f0-118">**PrepareSubmit** é usado para manipular mensagens que têm o sinalizador MSGFLAG_RESEND definido em sua **propriedade PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="688f0-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="688f0-119">MSGFLAG_RESEND é definido para mensagens que incluem uma solicitação a serem reente quando uma transmissão inicial falha.</span><span class="sxs-lookup"><span data-stu-id="688f0-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="688f0-120">**PrepareSubmit** determina quais dos destinatários na lista de destinatários receberam com êxito a mensagem e quais não receberam.</span><span class="sxs-lookup"><span data-stu-id="688f0-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="688f0-121">Para acessar a lista de **destinatários, PrepareSubmit** chama o método [IMessage::GetRecipientTable da](imessage-getrecipienttable.md) mensagem.</span><span class="sxs-lookup"><span data-stu-id="688f0-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="688f0-122">Para recuperar os dados do destinatário, **PrepareSubmit** chama o método [IMAPITable::QueryRows da](imapitable-queryrows.md) tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="688f0-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="688f0-123">Para cada linha na tabela, **PrepareSubmit** verifica a **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) e toma uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="688f0-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="688f0-124">Se o MAPI_SUBMITTED sinalizador estiver definido, **PrepareSubmit** limpará o sinalizador e definirá a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como FALSE.</span><span class="sxs-lookup"><span data-stu-id="688f0-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="688f0-125">Se o MAPI_SUBMITTED sinalizador não estiver definido, **PrepareSubmit** PR_RECIPIENT_TYPE para MAPI_P1 e define PR_RESPONSIBILITY **como** TRUE. </span><span class="sxs-lookup"><span data-stu-id="688f0-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="688f0-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="688f0-126">Notes to callers</span></span>

<span data-ttu-id="688f0-127">Antes de chamar **PrepareSubmit,** certifique-se de ter chamado o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) e defina o sinalizador NOTIFY_READYTOSEND no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="688f0-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="688f0-128">A **chamada SpoolerNotify** deve ser feita uma vez por sessão antes da chamada para **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="688f0-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="688f0-129">**O SpoolerNotify** sincroniza o spooler MAPI e garante que todos os provedores de transporte necessários estejam conectados e seus tipos de endereço estejam registrados.</span><span class="sxs-lookup"><span data-stu-id="688f0-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="688f0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="688f0-130">See also</span></span>



[<span data-ttu-id="688f0-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="688f0-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="688f0-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="688f0-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="688f0-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="688f0-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

