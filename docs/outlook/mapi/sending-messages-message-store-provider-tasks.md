---
title: Enviar tarefas do provedor do armazenamento de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de29707c7a257ea0e7ad658622d2a3054487f8b5
ms.sourcegitcommit: adcf409d56b6cb25be6117f09794defa41ad6c0f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2019
ms.locfileid: "37495303"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Enviar Mensagens: Tarefas do Provedor do Armazenamento de Mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de armazenamento de mensagens se envolve com o processo de envio de mensagens quando um cliente chama o método [IMessage::SubmitMessage da](imessage-submitmessage.md) mensagem. Se várias mensagens devem ser enviadas, o armazenamento de mensagens deve enviá-las na mesma ordem que o cliente usou para suas **chamadas SubmitMessage.** 
  
O provedor de armazenamento de mensagens determina se deve ou não envolver o spooler MAPI. Se o provedor de armazenamento de mensagens não estiver fortemente unido, a mensagem exigirá pré-processamento ou o armazenamento e o transporte fortemente a seguir não poderão manipular todos os destinatários, o spooler MAPI deverá estar envolvido. 
  
O procedimento a seguir descreve as tarefas necessárias de um provedor de armazenamento de mensagens para enviar uma mensagem. 
  
**Em IMessage::SubmitMessage, o provedor de armazenamento de mensagens:**
  
1. Chama [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) se MSGFLAG_RESEND mensagem tiver o sinalizador MSGFLAG_RESEND definido em sua propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e retornar quaisquer erros para o cliente. **PrepareSubmit** verifica **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário na lista de destinatários da mensagem.
    
   - Se o sinalizador MAPI_SUBMITTED estiver definido, indicando que o destinatário não recebeu a mensagem original, **PrepareSubmit** limpará o sinalizador e definirá a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como TRUE. 
    
   - Se o sinalizador MAPI_SUBMITTED não estiver definido, indicando que o destinatário recebeu a mensagem original, **PrepareSubmit** altera a propriedade **PR_RECIPIENT_TYPE** para MAPI_P1 e define a propriedade **PR_RESPONSIBILITY** como TRUE e retorna qualquer erro gerado pelo **PrepareSubmit** para o cliente. 
    
2. Define o MSGFLAG_SUBMIT sinalizador na propriedade PR_MESSAGE_FLAGS **mensagem.** 
    
3. Garante que haja uma  coluna para PR_RESPONSIBILITY na tabela de destinatários e a define como FALSE para indicar que nenhum transporte assume a responsabilidade pela transmissão da mensagem. 
    
4. Define a data e a hora de origem **na propriedade PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Chama [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) para: 
    
   - Expanda todas as listas de distribuição pessoais e destinatários personalizados e substitua todos os nomes de exibição alterados por seus nomes originais.
   - Remover nomes duplicados.
   - Verifique se há qualquer pré-processamento necessário e, se for necessário, de definir o sinalizador NEEDS_PREPROCESSING e a propriedade **PR_PREPROCESS** ([PidTagPreprocess),](pidtagpreprocess-canonical-property.md)uma propriedade reservada para MAPI. 
   - De definida NEEDS_SPOOLER sinalizador se o armazenamento de mensagens estiver fortemente unido a um transporte e não puder manipular todos os destinatários. 
    
6. Executa as seguintes tarefas se o sinalizador NEEDS_PREPROCESSING mensagem estiver definido:
    
   - Coloca a mensagem na fila de saída com o SUBMITFLAG_PREPROCESS bit definido na propriedade **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags).](pidtagsubmitflags-canonical-property.md)
   - Notifica o spooler MAPI de que a fila foi alterada.
   - Retorna o controle para o cliente, e o fluxo de mensagens continua no spooler MAPI. 
   - O spooler MAPI executa as seguintes tarefas:
     - Bloqueia a mensagem chamando IMsgStore::SetLockState. 
     - Executa o pré-processamento necessário chamando todas as funções de pré-processamento na ordem de registro. Provedores de transporte chamam IMAPISupport::RegisterPreprocessor para registrar funções de pré-processamento. 
     - Chama IMessage::SubmitMessage na mensagem aberta para indicar ao armazenamento de mensagens que o pré-processamento foi concluído.

<br/>

As duas etapas a seguir ocorrerão no processo do cliente se não houver pré-processamento e quando o spooler MAPI chamar **SubmitMessage** se houver pré-processamento. 

**O provedor de armazenamento de mensagens:**

1. Executa as seguintes tarefas se o armazenamento de mensagens estiver fortemente unido a um transporte e o sinalizador NEEDS_SPOOLER foi retornado de [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Trata todos os destinatários que ele pode manipular.
   - Define a **PR_RESPONSIBILITY** propriedade como TRUE para todos os destinatários que ela manipular. 
   - Executa as seguintes tarefas se todos os destinatários são conhecidos por esse transporte e armazenamento fortemente próximos:
     - Chama IMAPISupport::CompleteMsg se a mensagem foi pré-processada ou se o provedor de armazenamento de mensagens deseja que o spooler MAPI conclua o processamento de mensagens, o que é recomendado para que ganchos de mensagens possam ser invocados. O fluxo de mensagens continua com o spooler MAPI conforme descrito no procedimento a seguir.  
     - Executa as seguintes tarefas se a mensagem não tiver sido pré-processada ou se o provedor do armazenamento de mensagens não quiser que o spooler MAPI conclua o processamento de mensagens:
       - Copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), se definida.
       - Exclui a mensagem se a PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) tiver sido definida como TRUE.
       - Desbloqueia a mensagem se ela estiver bloqueada.
       - Retorna ao cliente. O fluxo de mensagens está concluído. 
   
2. Executa as seguintes tarefas se o armazenamento de mensagens não estiver fortemente unido a um transporte, nem todos os destinatários eram conhecidos no armazenamento de mensagens ou o sinalizador de NEEDS_SPOOLER está definido:
    
   - Coloca a mensagem na fila de saída sem definir o SUBMITFLAG_PREPROCESS bit na **propriedade PR_SUBMIT_FLAGS** saída. 
   - Notifica o spooler MAPI de que a fila de saída foi alterada gerando uma notificação de tabela. 
   - Retorna ao cliente, e o fluxo de mensagens continua com um conjunto de tarefas executadas pelo spooler MAPI.
    
Quando uma mensagem deve ser manipulada pelo spooler MAPI, o provedor de armazenamento de mensagens define a propriedade PR_SUBMIT_FLAGS **da** mensagem como SUBMITFLAG_LOCKED. O SUBMITFLAG_LOCKED sinalizador indica que o spooler MAPI travadau a mensagem para seu uso exclusivo. O outro valor para **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, é definido quando a mensagem exige o pré-processamento por uma ou mais funções de pré-processador registradas por um provedor de transporte. 
  

