---
title: Envio de tarefas do provedor de armazenamento de mensagens de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8bfa5709dede4a9501d261e0f495acbc0894b470
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770365"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Enviar mensagens: tarefas do provedor do repositório de mensagens

**Aplica-se a**: Outlook 
  
Um provedor de armazenamento de mensagem obtém envolvido com a mensagem enviando processo quando um cliente chama o método de [IMessage::SubmitMessage](imessage-submitmessage.md) da mensagem. Se várias mensagens devem ser enviados, o armazenamento de mensagens deve enviá-los na mesma ordem em que o cliente usado para suas chamadas **SubmitMessage** . 
  
O provedor de armazenamento de mensagem determina se ou não envolvem o spooler MAPI. Se o provedor de armazenamento de mensagem não está intimamente ligado, a mensagem requer a pré-processamento, ou o repositório de ligação estreita e o transporte não podem lidar com todos os destinatários, o MAPI spooler deve estar envolvido. 
  
O procedimento a seguir descreve as tarefas necessárias de um provedor de armazenamento de mensagem para enviar uma mensagem. 
  
**Provedor de armazenamento do IMessage::SubmitMessage no, a mensagem**:
  
1. Chama [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) se a mensagem tem o sinalizador MSGFLAG_RESEND definido em sua propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e retorna quaisquer erros para o cliente. **PrepareSubmit** verifica a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário na lista de destinatários da mensagem.
    
   - Se o sinalizador MAPI_SUBMITTED for definido, indicando que o destinatário não recebeu a mensagem original, o **PrepareSubmit** limpa o sinalizador e define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como TRUE. 
    
   - Se o sinalizador MAPI_SUBMITTED não estiver definido, indicando que o destinatário tenha recebido a mensagem original, **PrepareSubmit** altera a propriedade **PR_RECIPIENT_TYPE** para MAPI_P1 e define a propriedade **PR_RESPONSIBILITY** como TRUE e retorna qualquer erro gerado pelo **PrepareSubmit** ao cliente. 
    
2. Define o sinalizador MSGFLAG_SUBMIT na propriedade **PR_MESSAGE_FLAGS** da mensagem. 
    
3. Certifica-se de que existe uma coluna para **PR_RESPONSIBILITY** na tabela de destinatário e define como FALSE para indicar que nenhum transporte possui de responsabilidade ainda presumida para transmitir a mensagem. 
    
4. Define a data e hora de origem na propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Chama [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) para: 
    
   - Expandir todas as listas de distribuição pessoal e destinatários personalizados e substitua todos os nomes de exibição alterados por seus nomes originais.
   - Remova nomes duplicados.
   - Verifique qualquer pré-processamento necessário e, se for necessário pré-processamento, defina o sinalizador NEEDS_PREPROCESSING e a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), uma propriedade reservados para MAPI. 
   - Defina o sinalizador NEEDS_SPOOLER se o armazenamento de mensagens está firmemente combinado com um transporte e ele não pode lidar com todos os destinatários. 
    
6. Se o sinalizador de mensagem NEEDS_PREPROCESSING estiver definido, executa as seguintes tarefas:
    
   - Coloca a mensagem na fila de saída com o bit SUBMITFLAG_PREPROCESS definido na propriedade **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)).
   - Notifica o spooler MAPI que a fila foi alterada.
   - Retorna o controle para o cliente e o fluxo de mensagens continua no spooler MAPI. 
   - O MAPI spooler executa as seguintes tarefas:
     - Bloqueia a mensagem chamando IMsgStore::SetLockState. 
     - Executa o needed pré-processamento chamando todas as funções pré-processamento na ordem de registro. Provedores de transporte chamarem IMAPISupport::RegisterPreprocessor para registrar as funções de pré-processamento. 
     - Chama IMessage::SubmitMessage na mensagem aberta para indicar ao repositório de mensagem que pré-processamento está concluído.

<br/>

As duas etapas a seguintes ocorrem no processo de cliente não se houve nenhum pré-processamento e quando o MAPI spooler chama **SubmitMessage** se há foi pré-processamento. 

**Provedor de armazenamento de mensagem**:

1. Se o armazenamento de mensagens está intimamente ligado a um transporte e o sinalizador NEEDS_SPOOLER foi retornado de [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md), executa as seguintes tarefas:
    
   - Trata quaisquer destinatários que pode manipular.
   - Define a propriedade **PR_RESPONSIBILITY** como TRUE para quaisquer destinatários que ele manipula. 
   - Se todos os destinatários são conhecidos como esse ligação estreita de armazenamento e o transporte, executa as seguintes tarefas:
     - Chama IMAPISupport::CompleteMsg se a mensagem foi pré-processado ou a mensagem o MAPI spooler para concluir o processamento de mensagens, que é recomendado para que as mensagens podem ser invocados ganchos de provedor quer armazenar. Fluxo de mensagens continua com o spooler MAPI, conforme descrito no procedimento a seguir.  
     - Se a mensagem não foi pré-processado ou o provedor de armazenamento de mensagem não deseja que o spooler MAPI para concluir o processamento de mensagens, executa as seguintes tarefas:
       - Cópias em que a mensagem para a pasta identificada pelo identificador de entrada na propriedade PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), se definida.
       - Exclui a mensagem se a propriedade PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) tiver sido definida como TRUE.
       - Desbloqueia a mensagem se ele estiver bloqueado.
       - Retorna para o cliente. Fluxo de mensagens é concluído. 
   
2. Se o armazenamento de mensagens não está intimamente ligado a um transporte, nem todos os destinatários eram conhecidos para o armazenamento de mensagens ou o sinalizador NEEDS_SPOOLER estiver definido, executa as seguintes tarefas:
    
   - Coloca a mensagem na fila de saída sem definir estará definido o bit SUBMITFLAG_PREPROCESS na propriedade **PR_SUBMIT_FLAGS** . 
   - Notifica o spooler MAPI que a fila de saída foi alterada gerando uma notificação de tabela. 
   - Continua a retorna para o cliente e o fluxo de mensagens com um conjunto de tarefas realizadas pelo spooler MAPI.
    
Quando uma mensagem é sejam manipuladas pelo MAPI spooler, o provedor de armazenamento de mensagem define a propriedade **PR_SUBMIT_FLAGS** da mensagem para SUBMITFLAG_LOCKED. O sinalizador SUBMITFLAG_LOCKED indica que o MAPI spooler tiver bloqueado a mensagem para seu uso exclusivo. O outro valor para **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, é definido quando a mensagem requer a pré-processamento por uma ou mais funções pré-processador registradas por um provedor de transporte. 
  

