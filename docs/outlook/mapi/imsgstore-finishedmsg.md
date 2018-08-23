---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589949"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="32a4f-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="32a4f-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="32a4f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32a4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32a4f-105">Permite que o provedor de armazenamento de mensagem executar o processamento em uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="32a4f-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="32a4f-106">Este método é chamado somente pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="32a4f-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="32a4f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32a4f-107">Parameters</span></span>

 <span data-ttu-id="32a4f-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32a4f-108">_ulFlags_</span></span>
  
> <span data-ttu-id="32a4f-109">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="32a4f-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="32a4f-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="32a4f-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="32a4f-111">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="32a4f-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="32a4f-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="32a4f-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="32a4f-113">[in] Um ponteiro para o identificador de entrada da mensagem a ser processado.</span><span class="sxs-lookup"><span data-stu-id="32a4f-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32a4f-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="32a4f-114">Return value</span></span>

<span data-ttu-id="32a4f-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="32a4f-115">S_OK</span></span> 
  
> <span data-ttu-id="32a4f-116">Processamento na mensagem enviada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="32a4f-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="32a4f-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="32a4f-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="32a4f-118">O provedor de armazenamento de mensagem não suporta o processamento da mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="32a4f-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="32a4f-119">Esse valor de erro será retornado se o chamador não é o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="32a4f-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32a4f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="32a4f-120">Remarks</span></span>

<span data-ttu-id="32a4f-121">O método **IMsgStore::FinishedMsg** realiza processamento em uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="32a4f-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="32a4f-122">Esse processamento pode envolver excluindo a mensagem, movê-lo para uma pasta diferente, ou ambas as ações.</span><span class="sxs-lookup"><span data-stu-id="32a4f-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="32a4f-123">O tipo de processamento depende se o **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) e as propriedades de **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) estão definidas.</span><span class="sxs-lookup"><span data-stu-id="32a4f-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="32a4f-124">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="32a4f-124">Notes to implementers</span></span>

<span data-ttu-id="32a4f-125">Na sua implementação do **FinishedMsg**, desbloquear a mensagem identificada pela _lpEntryID_ e execute o processamento apropriado.</span><span class="sxs-lookup"><span data-stu-id="32a4f-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="32a4f-126">A mensagem de destino sempre será bloqueada; o MAPI spooler nunca passa o identificador de entrada de mensagem desbloqueada para **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="32a4f-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="32a4f-127">É possível que nem **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** estiver definida, ambos são definidos ou um ou outro estiver definido.</span><span class="sxs-lookup"><span data-stu-id="32a4f-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="32a4f-128">A tabela a seguir descreve a ação que deve ser adotada com base nas configurações:</span><span class="sxs-lookup"><span data-stu-id="32a4f-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32a4f-129">Se nenhuma propriedade for definida:</span><span class="sxs-lookup"><span data-stu-id="32a4f-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="32a4f-130">Deixe a mensagem na pasta da qual ela foi enviada (normalmente a caixa de saída).</span><span class="sxs-lookup"><span data-stu-id="32a4f-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="32a4f-131">Se ambas as propriedades são definidas:</span><span class="sxs-lookup"><span data-stu-id="32a4f-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="32a4f-132">Move a mensagem para a pasta indicada, se desejado e, em seguida, excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="32a4f-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="32a4f-133">Se estiver definido PR_SENTMAIL_ENTRYID:</span><span class="sxs-lookup"><span data-stu-id="32a4f-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="32a4f-134">Move a mensagem para a pasta indicada.</span><span class="sxs-lookup"><span data-stu-id="32a4f-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="32a4f-135">Se estiver definido PR_DELETE_AFTER_SUBMIT:</span><span class="sxs-lookup"><span data-stu-id="32a4f-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="32a4f-136">Exclua a mensagem.</span><span class="sxs-lookup"><span data-stu-id="32a4f-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="32a4f-137">Depois de executar qualquer ação é apropriada, chame o método de [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) .</span><span class="sxs-lookup"><span data-stu-id="32a4f-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32a4f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="32a4f-138">See also</span></span>



[<span data-ttu-id="32a4f-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="32a4f-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="32a4f-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="32a4f-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

