---
title: Enviando mensagens MAPI Spooler tarefas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ff40eddf63e67f45495e90c1a960e45b7cc6cfb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770368"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="822c5-103">Enviar mensagens: tarefas do spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="822c5-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="822c5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="822c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="822c5-105">O MAPI spooler está envolvido no processo de transmissão de mensagem quando o armazenamento de mensagens não está firmemente combinado com um provedor de transporte, quando o repositório de ligação estreita e o transporte não podem tratar um destinatário e quando a mensagem requer pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="822c5-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="822c5-106">**Depois de qualquer necessário pré-processamento, o MAPI spooler executa as seguintes etapas:**</span><span class="sxs-lookup"><span data-stu-id="822c5-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="822c5-107">Se a mensagem não estiver bloqueada, bloqueia a mensagem usando o método [IMsgStore::SetLockState](imsgstore-setlockstate.md) .</span><span class="sxs-lookup"><span data-stu-id="822c5-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="822c5-108">Tem o provedor de transporte para enviar a mensagem a todos os destinatários cuja propriedade seu **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) é definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="822c5-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="822c5-109">Chama a função adequada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpar qualquer informação adicional que foi adicionada à mensagem para uso durante a pré-processamento se tiver sido definida a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="822c5-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="822c5-110">Essa função é especificada quando o provedor de transporte registra sua função pré-processador.</span><span class="sxs-lookup"><span data-stu-id="822c5-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="822c5-111">Chama o método [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="822c5-111">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method.</span></span> <span data-ttu-id="822c5-112">Em **FinishedMsg**, o provedor de armazenamento de mensagem:</span><span class="sxs-lookup"><span data-stu-id="822c5-112">In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="822c5-113">Desbloqueia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="822c5-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="822c5-114">Chama o método [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) para executar o processamento de saída do gancho se existir um provedor de mensagens do gancho.</span><span class="sxs-lookup"><span data-stu-id="822c5-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="822c5-115">Ele, em seguida, copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se não foram substituídas por uma mensagem gancho provedor do enviadas processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="822c5-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="822c5-116">Finalmente, ele exclui a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="822c5-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

