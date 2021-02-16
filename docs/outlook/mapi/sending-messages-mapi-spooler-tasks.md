---
title: Enviar mensagens tarefas do Spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420196"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Enviar Mensagens: Tarefas do Spooler MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O spooler MAPI está envolvido no processo de transmissão de mensagens quando o armazenamento de mensagens não está fortemente unido a um provedor de transporte, quando o armazenamento e o transporte fortemente juntos não podem manipular um destinatário e quando a mensagem requer pré-processamento.
  
 **Após qualquer pré-processamento necessário, o spooler MAPI executa as seguintes etapas:**
  
1. Se a mensagem não estiver bloqueada, bloqueia a mensagem usando o [método IMsgStore::SetLockState.](imsgstore-setlockstate.md) 
    
2. Faz com que o provedor de transporte envie a mensagem para todos os **destinatários** que têm sua propriedade PR_RESPONSIBILITY ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como FALSE. 
    
3. Chama a função apropriada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpar quaisquer informações adicionais que foram adicionadas à mensagem para uso durante o pré-processamento se a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) tiver sido definida. Esta função é especificada quando o provedor de transporte registra sua função de pré-processador. 
    
4. Chama [o método IMsgStore::FinishedMsg.](imsgstore-finishedmsg.md) Em **FinishedMsg**, o provedor de armazenamento de mensagens:
    
  - Desbloqueia a mensagem.
    
  - Chama o [método IMAPISupport::D oSentMail](imapisupport-dosentmail.md) para executar o processamento de gancho de saída se houver um provedor de gancho de mensagens. Em seguida, copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se não for sobresserida pelo processamento de mensagens enviado por um provedor de gancho de mensagens. Por fim, ele excluirá a mensagem **se a PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como TRUE. 
    

