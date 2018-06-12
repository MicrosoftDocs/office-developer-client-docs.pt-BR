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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767293"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="9ce9e-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="9ce9e-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="9ce9e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ce9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ce9e-105">Prepara uma mensagem para o envio para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9ce9e-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9ce9e-106">Parameters</span></span>

 <span data-ttu-id="9ce9e-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9ce9e-107">_lpMessage_</span></span>
  
> <span data-ttu-id="9ce9e-108">[in] Um ponteiro para a mensagem para preparar.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="9ce9e-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ce9e-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="9ce9e-110">[além, out] Na entrada, o parâmetro _lpulFlags_ é reservado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="9ce9e-111">Na saída, _lpulFlags_ deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ce9e-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9ce9e-112">Return value</span></span>

<span data-ttu-id="9ce9e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ce9e-113">S_OK</span></span> 
  
> <span data-ttu-id="9ce9e-114">A mensagem foi preparada com êxito.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ce9e-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="9ce9e-115">Remarks</span></span>

<span data-ttu-id="9ce9e-116">O método **IMAPISupport::PrepareSubmit** é implementado para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9ce9e-117">Provedores de armazenamento de mensagem chamarem **PrepareSubmit** em sua implementação do método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar uma mensagem para o envio para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="9ce9e-118">**PrepareSubmit** é usado para tratar mensagens que têm o sinalizador MSGFLAG_RESEND definido em sua propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9ce9e-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="9ce9e-119">MSGFLAG_RESEND é definida para mensagens que incluem uma solicitação a ser reenviado quando uma transmissão inicial falha.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="9ce9e-120">**PrepareSubmit** determina qual dos destinatários na lista de destinatários com êxito recebeu a mensagem e que não especificou.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="9ce9e-121">Para acessar a lista de destinatários, **PrepareSubmit** chama o método de [IMessage::GetRecipientTable](imessage-getrecipienttable.md) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="9ce9e-122">Para recuperar os dados de destinatário, **PrepareSubmit** chama o método [IMAPITable:: QueryRows](imapitable-queryrows.md) de destinatário da tabela.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="9ce9e-123">Para cada linha na tabela, **PrepareSubmit** verifica a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) e usa uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="9ce9e-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="9ce9e-124">Se o sinalizador MAPI_SUBMITTED estiver definido, o **PrepareSubmit** limpa o sinalizador e define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como FALSE.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="9ce9e-125">Se o sinalizador MAPI_SUBMITTED não estiver definido, o **PrepareSubmit** **PR_RECIPIENT_TYPE** é alterado para MAPI_P1 e define **PR_RESPONSIBILITY** como TRUE.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="9ce9e-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9ce9e-126">Notes to callers</span></span>

<span data-ttu-id="9ce9e-127">Antes de chamar **PrepareSubmit**, certifique-se de que você chamou o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) e definir o sinalizador NOTIFY_READYTOSEND no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9ce9e-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="9ce9e-128">A chamada **SpoolerNotify** deve ser feita uma vez por sessão antes da chamada para **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="9ce9e-129">**SpoolerNotify** sincroniza o MAPI spooler e garante que todos os provedores de transporte needed estiver conectados e seus tipos de endereço são registrados.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ce9e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ce9e-130">See also</span></span>



[<span data-ttu-id="9ce9e-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="9ce9e-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="9ce9e-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9ce9e-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="9ce9e-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ce9e-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

