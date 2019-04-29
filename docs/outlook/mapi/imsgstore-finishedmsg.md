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
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427084"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="6a3fc-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="6a3fc-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="6a3fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a3fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a3fc-105">Permite que o provedor de repositório de mensagens realize o processamento em uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="6a3fc-106">Este método é chamado apenas pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="6a3fc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a3fc-107">Parameters</span></span>

 <span data-ttu-id="6a3fc-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a3fc-108">_ulFlags_</span></span>
  
> <span data-ttu-id="6a3fc-109">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6a3fc-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6a3fc-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="6a3fc-111">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="6a3fc-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6a3fc-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6a3fc-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="6a3fc-113">no Um ponteiro para o identificador de entrada da mensagem a ser processada.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a3fc-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6a3fc-114">Return value</span></span>

<span data-ttu-id="6a3fc-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a3fc-115">S_OK</span></span> 
  
> <span data-ttu-id="6a3fc-116">O processamento da mensagem enviada foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="6a3fc-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6a3fc-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6a3fc-118">O provedor de repositório de mensagens não dá suporte ao processamento de mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="6a3fc-119">Este valor de erro será retornado se o chamador não for o MAPI spooler.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a3fc-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a3fc-120">Remarks</span></span>

<span data-ttu-id="6a3fc-121">O método **IMsgStore:: FinishedMsg** executa o processamento em uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="6a3fc-122">Esse processamento pode envolver a exclusão da mensagem, movê-la para uma pasta diferente ou ambas as ações.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="6a3fc-123">O tipo de processamento depende se as propriedades **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) e **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) estão definidas.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6a3fc-124">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="6a3fc-124">Notes to implementers</span></span>

<span data-ttu-id="6a3fc-125">Em sua implementação do **FinishedMsg**, desbloqueie a mensagem identificada por _lpEntryID_ e execute o processamento apropriado.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="6a3fc-126">A mensagem de destino sempre será bloqueada; o spooler MAPI nunca passa o identificador de entrada de uma mensagem desbloqueada para **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="6a3fc-127">É possível que nem **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** estejam definidos, ambos estejam definidos ou um ou outro esteja definido.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="6a3fc-128">A tabela a seguir descreve a ação que deve ser executada com base nas configurações:</span><span class="sxs-lookup"><span data-stu-id="6a3fc-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a3fc-129">Se nenhuma propriedade for definida:</span><span class="sxs-lookup"><span data-stu-id="6a3fc-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="6a3fc-130">Deixe a mensagem na pasta a partir da qual ela foi enviada (normalmente, a).</span><span class="sxs-lookup"><span data-stu-id="6a3fc-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="6a3fc-131">Se ambas as propriedades estiverem definidas:</span><span class="sxs-lookup"><span data-stu-id="6a3fc-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="6a3fc-132">Mova a mensagem para a pasta indicada, se desejado, e, em seguida, exclua-a.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="6a3fc-133">Se PR_SENTMAIL_ENTRYID estiver definido:</span><span class="sxs-lookup"><span data-stu-id="6a3fc-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="6a3fc-134">Mova a mensagem para a pasta indicada.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="6a3fc-135">Se PR_DELETE_AFTER_SUBMIT estiver definido:</span><span class="sxs-lookup"><span data-stu-id="6a3fc-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="6a3fc-136">Exclua a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6a3fc-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="6a3fc-137">Depois de ter feito qualquer ação apropriada, chame o método [IMAPISupport::D osentmail](imapisupport-dosentmail.md) .</span><span class="sxs-lookup"><span data-stu-id="6a3fc-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a3fc-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a3fc-138">See also</span></span>



[<span data-ttu-id="6a3fc-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="6a3fc-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="6a3fc-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6a3fc-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

