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
# <a name="sending-messages-mapi-spooler-tasks"></a>Enviar mensagens: tarefas do spooler MAPI

  
  
**Aplica-se a**: Outlook 
  
O MAPI spooler está envolvido no processo de transmissão de mensagem quando o armazenamento de mensagens não está firmemente combinado com um provedor de transporte, quando o repositório de ligação estreita e o transporte não podem tratar um destinatário e quando a mensagem requer pré-processamento.
  
 **Depois de qualquer necessário pré-processamento, o MAPI spooler executa as seguintes etapas:**
  
1. Se a mensagem não estiver bloqueada, bloqueia a mensagem usando o método [IMsgStore::SetLockState](imsgstore-setlockstate.md) . 
    
2. Tem o provedor de transporte para enviar a mensagem a todos os destinatários cuja propriedade seu **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) é definida como FALSE. 
    
3. Chama a função adequada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpar qualquer informação adicional que foi adicionada à mensagem para uso durante a pré-processamento se tiver sido definida a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)). Essa função é especificada quando o provedor de transporte registra sua função pré-processador. 
    
4. Chama o método [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) . Em **FinishedMsg**, o provedor de armazenamento de mensagem:
    
  - Desbloqueia a mensagem.
    
  - Chama o método [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) para executar o processamento de saída do gancho se existir um provedor de mensagens do gancho. Ele, em seguida, copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se não foram substituídas por uma mensagem gancho provedor do enviadas processamento de mensagens. Finalmente, ele exclui a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como TRUE. 
    

