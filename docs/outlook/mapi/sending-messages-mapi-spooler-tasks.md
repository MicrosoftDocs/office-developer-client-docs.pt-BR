---
title: Enviando tarefas de spooler MAPI de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339673"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="7107b-103">Enviar mensagens: tarefas do spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="7107b-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="7107b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7107b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7107b-105">O spooler MAPI está envolvido no processo de transmissão de mensagens quando o repositório de mensagens não está rigidamente acoplado a um provedor de transporte, quando o armazenamento e transporte rigidamente acoplados não conseguem lidar com um destinatário e quando a mensagem requer o pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="7107b-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="7107b-106">**Após qualquer pré-processamento necessário, o spooler MAPI realiza as seguintes etapas:**</span><span class="sxs-lookup"><span data-stu-id="7107b-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="7107b-107">Se a mensagem não estiver bloqueada, bloqueia a mensagem usando o método [IMsgStore::](imsgstore-setlockstate.md) setlockstate.</span><span class="sxs-lookup"><span data-stu-id="7107b-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="7107b-108">O provedor de transporte envia a mensagem para todos os destinatários que têm sua propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como false.</span><span class="sxs-lookup"><span data-stu-id="7107b-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="7107b-109">Chama a função apropriada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpar as informações adicionais que foram adicionadas à mensagem para uso durante o pré-processamento, se a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="7107b-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="7107b-110">Essa função é especificada quando o provedor de transporte registra sua função de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="7107b-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="7107b-111">Chama o método [IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="7107b-111">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method.</span></span> <span data-ttu-id="7107b-112">No **FinishedMsg**, o provedor do repositório de mensagens:</span><span class="sxs-lookup"><span data-stu-id="7107b-112">In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="7107b-113">Desbloqueia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="7107b-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="7107b-114">Chama o método [IMAPISupport::D osentmail](imapisupport-dosentmail.md) para executar o processamento de gancho de saída se um provedor de conexão de mensagens existir.</span><span class="sxs-lookup"><span data-stu-id="7107b-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="7107b-115">Em seguida, ele copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se não for substituída por um provedor de conexão de mensagens enviado.</span><span class="sxs-lookup"><span data-stu-id="7107b-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="7107b-116">Por fim, ele excluirá a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como true.</span><span class="sxs-lookup"><span data-stu-id="7107b-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

