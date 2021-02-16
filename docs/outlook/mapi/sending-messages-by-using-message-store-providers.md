---
title: Enviar mensagens usando provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b34714a230adb44417624d149d34ed6a14a2dfa5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437606"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Enviar mensagens usando provedores do repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de armazenamento de mensagens não são obrigados a dar suporte a envios de mensagens de saída (ou seja, a capacidade dos aplicativos clientes usarem o provedor de armazenamento de mensagens para enviar mensagens). Os aplicativos cliente precisam usar um armazenamento de mensagens durante o envio de mensagens, porque os dados da mensagem devem ser armazenados em algum lugar entre o momento em que o usuário terminou de retorá-la e a hora em que o spooler MAPI entrega a mensagem a um provedor de transporte para envio ao sistema de mensagens subjacente. Se seu provedor de armazenamento de mensagens não suportar envios de mensagens de saída, ele não poderá ser usado como o armazenamento de mensagens padrão.
  
Para dar suporte ao envio de mensagens, seu provedor de armazenamento de mensagens deve fazer o seguinte:
  
- Implemente uma fila de mensagens de saída.
    
- Suporte ao [método IMessage::SubmitMessage](imessage-submitmessage.md) em objetos de mensagem criados no armazenamento de mensagens. 
    
- Suporte aos métodos **IMsgStore** específicos para o spooler MAPI: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)e [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
O **método SetLockState** é importante para interoperação adequada entre o spooler MAPI e os clientes. Quando o spooler MAPI chama **SetLockState** em uma mensagem de saída, o provedor de armazenamento de mensagens não deve permitir que os clientes abram a mensagem. Se um cliente tentar abrir uma mensagem bloqueada pelo spooler MAPI, o provedor de armazenamento de mensagens deverá retornar MAPI_E_NO_ACCESS. O estado bloqueado de uma mensagem não precisa ser persistente no caso de o armazenamento ser desligado enquanto a mensagem é bloqueada pelo spooler MAPI. 
  
Independentemente de o spooler MAPI ter bloqueado uma mensagem de saída, o provedor de armazenamento de mensagens não deve permitir que uma mensagem na fila de mensagens de saída seja aberta para escrita. Se um cliente chamar o método [IMSgStore::OpenEntry](imsgstore-openentry.md) em uma mensagem de saída com o sinalizador MAPI_MODIFY, a chamada falhará e retornará MAPI_E_SUBMITTED. Se um aplicativo cliente chamar **OpenEntry** em uma mensagem de saída com o sinalizador MAPI_BEST_ACCESS, o provedor de armazenamento de mensagens deverá permitir acesso somente leitura à mensagem. 
  
Quando uma mensagem deve ser manipulada pelo spooler MAPI, o provedor de armazenamento de mensagens define a propriedade **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) da mensagem como SUBMITFLAG_LOCKED. O SUBMITFLAG_LOCKED valor indica que o spooler MAPI travadau a mensagem para seu uso exclusivo. O outro valor para **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, é definido quando a mensagem exige pré-processamento por uma ou mais funções de pré-processador registradas por um provedor de transporte.
  
Os procedimentos a seguir descrevem como o armazenamento de mensagens, o transporte e o spooler MAPI interagem para enviar uma mensagem de um cliente para um ou mais destinatários. 
  
O aplicativo cliente chama o [método IMessage::SubmitMessage.](imessage-submitmessage.md) Em **SubmitMessage**, o provedor de armazenamento de mensagens faz o seguinte:
  
1. Chama [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). Se MAPI retornar um erro, o provedor de armazenamento de mensagens retornará esse erro para o cliente.
    
2. Define o MSGFLAG_SUBMIT bit **na propriedade PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
    
3. Garante que haja uma coluna para a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) na tabela de destinatários e a define como FALSE para indicar que nenhum transporte assume a responsabilidade pela transmissão da mensagem.
    
4. Define a data e a hora de origem **na propriedade PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Chama [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) para fazer o seguinte: 
    
    1. Expanda todas as listas de distribuição pessoais e destinatários personalizados e substitua todos os nomes de exibição alterados por seus nomes originais.
        
    2. Remover nomes duplicados.
        
    3. Verifique se há qualquer pré-processamento necessário e, se o pré-processamento for necessário, de definir o sinalizador NEEDS_PREPROCESSING e a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), que é reservado para MAPI. 
        
    4. De definida NEEDS_SPOOLER sinalizador se o armazenamento de mensagens estiver fortemente unido a um transporte e não puder manipular todos os destinatários. 
    
6. Executa as seguintes tarefas se o sinalizador NEEDS_PREPROCESSING mensagem estiver definido:
    
    1. Coloca a mensagem na fila de saída com o SUBMITFLAG_PREPROCESS bit definido na **propriedade PR_SUBMIT_FLAGS** saída. 
        
    2. Notifica o spooler MAPI de que a fila foi alterada.
        
    3. Retorna o controle para o cliente, e o fluxo de mensagens continua no spooler MAPI. O spooler MAPI executa as seguintes tarefas: 
    
       1. Bloqueia a mensagem chamando [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Executa o pré-processamento necessário chamando todas as funções de pré-processamento na ordem de registro. Provedores de transporte chamam [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar funções de pré-processamento. 
            
       3. Chama [IMessage::SubmitMessage](imessage-submitmessage.md) na mensagem aberta para indicar ao armazenamento de mensagens que o pré-processamento está concluído. 
    
Se não houve pré-processamento ou se houve pré-processamento e o spooler MAPI chamado **SubmitMessage**, o provedor de armazenamento de mensagens faz o seguinte no processo do cliente: 
  
- Executa as seguintes tarefas se o armazenamento de mensagens estiver fortemente unido a um transporte e o sinalizador NEEDS_SPOOLER foi retornado de [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Trata todos os destinatários que ele pode manipular.
    
   - Define a **PR_RESPONSIBILITY** propriedade como TRUE para todos os destinatários que ela manipular. 
    
   - Executa as seguintes tarefas se todos os destinatários são conhecidos por esse transporte e armazenamento fortemente próximos: 
    
     - Chama [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) se a mensagem foi pré-processada ou se o provedor de armazenamento de mensagens deseja que o spooler MAPI conclua o processamento de mensagens. O fluxo de mensagens continua com o spooler MAPI. 
    
     - Executa as seguintes tarefas se a mensagem não tiver sido pré-processada ou se o provedor de armazenamento de mensagens não quiser que o spooler MAPI conclua o processamento de mensagens:
    
       1. Copia a mensagem para a pasta identificada pelo identificador de entrada na **propriedade PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se definida.
            
       2. Exclui a mensagem se a **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como TRUE.
            
       3. Desbloqueia a mensagem se ela estiver bloqueada.
            
       4. Retorna ao cliente. O fluxo de mensagens está concluído.
    
  - Executa as seguintes tarefas se a mensagem foi pré-processada ou se o provedor deseja que o spooler MAPI conclua o processamento de mensagens:
    
    1. Chama [IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Continua o fluxo de mensagens com o spooler MAPI. Para obter mais informações, consulte [Enviando Mensagens: Tarefas do Spooler MAPI.](sending-messages-mapi-spooler-tasks.md)
    
  - Executa as seguintes tarefas se a mensagem não tiver sido pré-processada ou se o provedor não quiser que o spooler conclua o processamento de mensagens:
    
    1. Copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID,** se definida. 
        
    2. Exclui a mensagem se a **PR_DELETE_AFTER_SUBMIT** propriedade tiver sido definida como TRUE. 
        
    3. Desbloqueia a mensagem se ela estiver bloqueada. 
        
    4. Retorna ao chamador. O fluxo de mensagens está concluído.
    
- Executa as seguintes tarefas se o armazenamento de mensagens não estiver fortemente unido a um transporte, nem todos os destinatários eram conhecidos no armazenamento de mensagens ou o sinalizador de NEEDS_SPOOLER está definido:
    
  1. Coloca a mensagem na fila de saída sem definir SUBMITFLAG_PREPROCESS bit na **propriedade PR_SUBMIT_FLAGS** saída. 
    
  2. Notifica o spooler MAPI de que a fila de saída foi alterada gerando uma notificação de tabela. 
    
  3. Retorna ao cliente, e o fluxo de mensagens continua com um conjunto de tarefas executadas pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também

- [Recursos do Armazenamento de Mensagens](message-store-features.md)

