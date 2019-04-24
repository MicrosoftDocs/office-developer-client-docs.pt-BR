---
title: Tarefas do provedor de armazenamento de mensagens de envio
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b65113e59b236b1f13596627a8669ae458f76369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338427"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Enviar mensagens: tarefas do provedor de repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de repositório de mensagens é envolvido com o processo de envio de mensagens quando um cliente chama o método [IMessage:: SubmitMessage](imessage-submitmessage.md) da mensagem. Se várias mensagens forem enviadas, o repositório de mensagens deverá enviá-las na mesma ordem em que o cliente usou para suas chamadas do **SubmitMessage** . 
  
O provedor de repositório de mensagens determina se o spooler MAPI deve ou não ser envolvedo. Se o provedor de repositório de mensagens não estiver rigidamente acoplado, a mensagem exigirá o pré-processamento, ou o transporte rigidamente acoplado e o transporte não poderão lidar com todos os destinatários, o spooler MAPI deverá estar envolvido. 
  
O procedimento a seguir descreve as tarefas necessárias para um provedor de armazenamento de mensagens para o envio de uma mensagem. 
  
**No IMessage:: SubmitMessage, o provedor do repositório de mensagens**:
  
1. Chama [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) se a mensagem tiver o sinalizador MSGFLAG_RESEND definido em sua propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e retornar qualquer erro para o cliente. **PrepareSubmit** verifica a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário na lista de destinatários da mensagem.
    
   - Se o sinalizador MAPI_SUBMITTED estiver definido, indicando que o destinatário não recebeu a mensagem original, **PrepareSubmit** limpa o sinalizador e define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como true. 
    
   - Se o sinalizador MAPI_SUBMITTED não estiver definido, indicando que o destinatário recebeu a mensagem original, **PrepareSubmit** altera a propriedade **PR_RECIPIENT_TYPE** para MAPI_P1 e define a propriedade **PR_RESPONSIBILITY** como true e retorna qualquer erro gerado pelo **PrepareSubmit** para o cliente. 
    
2. Define o sinalizador MSGFLAG_SUBMIT na propriedade **PR_MESSAGE_FLAGS** da mensagem. 
    
3. Verifica se há uma coluna para **PR_RESPONSIBILITY** na tabela de destinatários e a define como false para indicar que nenhum transporte tem a responsabilidade assumida por transmitir a mensagem. 
    
4. Define a data e a hora da origem na propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Chama [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) : 
    
   - Expanda todas as listas de distribuição pessoal e destinatários personalizados e substitua todos os nomes de exibição alterados por seus nomes originais.
   - Remover nomes duplicados.
   - Verifique se há algum pré-processamento necessário e se o pré-processamento é necessário, defina o sinalizador NEEDS_PREPROCESSING e a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), uma propriedade reservada para MAPI. 
   - Defina o sinalizador NEEDS_SPOOLER se o repositório de mensagens estiver rigidamente acoplado a um transporte e não puder lidar com todos os destinatários. 
    
6. Executa as seguintes tarefas se o sinalizador de mensagem NEEDS_PREPROCESSING estiver definido:
    
   - Coloca a mensagem na fila de saída com o conjunto de bits SUBMITFLAG_PREPROCESS na propriedade **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)).
   - Notifica o spooler MAPI de que a fila foi alterada.
   - Retorna o controle ao cliente e o fluxo de mensagens continua no spooler MAPI. 
   - O spooler MAPI realiza as seguintes tarefas:
     - Bloqueia a mensagem chamando IMsgStore:: setLockstate. 
     - Realiza o pré-processamento necessário chamando todas as funções de pré-processamento na ordem de registro. Os provedores de transporte chamam IMAPISupport:: RegisterPreprocessor para registrar funções de pré-processamento. 
     - Chama IMessage:: SubmitMessage na mensagem aberta para indicar ao repositório de mensagens que o pré-processamento está completo.

<br/>

As duas etapas a seguir ocorrem no processo de cliente, se não houver pré-processamento, e quando o spooler MAPI chamar **SubmitMessage** se houver pré-processamento. 

**O provedor do repositório de mensagens**:

1. Realiza as seguintes tarefas se o repositório de mensagens estiver rigidamente acoplado a um transporte e o sinalizador NEEDS_SPOOLER retornado de [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md):
    
   - Cuida de qualquer destinatário que possa lidar.
   - Define a propriedade **PR_RESPONSIBILITY** como true para todos os destinatários que ele manipula. 
   - Realiza as seguintes tarefas se todos os destinatários forem conhecidos por esse transporte e transporte rigidamente acoplados:
     - Chama IMAPISupport:: CompleteMsg se a mensagem tiver sido preprocessada ou se o provedor de repositório de mensagens quiser que o spooler MAPI conclua o processamento de mensagens, o que é recomendado para que os ganchos de mensagens possam ser chamados. O fluxo de mensagens continua com o spooler MAPI, conforme descrito no procedimento a seguir.  
     - Realiza as seguintes tarefas se a mensagem não tiver sido preprocessada ou se o provedor do repositório de mensagens não quiser que o spooler MAPI Complete o processamento de mensagens:
       - Copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), se definida.
       - Exclui a mensagem se a propriedade PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) tiver sido definida como TRUE.
       - Desbloqueia a mensagem se estiver bloqueada.
       - Retorna ao cliente. O fluxo de mensagens foi concluído. 
   
2. Realiza as seguintes tarefas se o repositório de mensagens não estiver rigidamente acoplado a um transporte, nem todos os destinatários foram conhecidos no repositório de mensagens ou se o sinalizador NEEDS_SPOOLER estiver definido:
    
   - Coloca a mensagem na fila de saída sem definir o bit SUBMITFLAG_PREPROCESS na propriedade **PR_SUBMIT_FLAGS** . 
   - Notifica o spooler MAPI de que a fila de saída foi alterada gerando uma notificação de tabela. 
   - Retorna ao cliente e o fluxo de mensagens continua com um conjunto de tarefas executadas pelo spooler MAPI.
    
Quando uma mensagem é manipulada pelo spooler MAPI, o provedor do repositório de mensagens define a propriedade **PR_SUBMIT_FLAGS** da mensagem como SUBMITFLAG_LOCKED. O sinalizador SUBMITFLAG_LOCKED indica que o spooler MAPI bloqueou a mensagem para seu uso exclusivo. O outro valor para **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, é definido quando a mensagem requer o pré-processamento por uma ou mais funções de pré-processador registradas por um provedor de transporte. 
  

