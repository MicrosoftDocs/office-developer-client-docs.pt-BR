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
  
Os provedores de repositórios de mensagens não são necessários para dar suporte a envios de mensagens de saída (ou seja, a capacidade de aplicativos clientes usarem o provedor de armazenamento de mensagens para enviar mensagens). Os aplicativos cliente precisam usar um repositório de mensagens durante o envio de mensagens, pois os dados da mensagem devem ser armazenados em algum lugar entre o momento em que o usuário tiver concluído a composição e a hora em que o spooler MAPI fornece a mensagem a um provedor de transporte envio para o sistema de mensagens subjacente. Se o seu provedor de repositório de mensagens não oferecer suporte a envios de mensagens de saída, ele não poderá ser usado como o repositório de mensagens padrão.
  
Para dar suporte ao envio de mensagens, seu provedor de repositório de mensagens deve fazer o seguinte:
  
- Implementar uma fila de mensagens de saída.
    
- Suporte para o método [IMessage:: SubmitMessage](imessage-submitmessage.md) em objetos Message criados no repositório de mensagens. 
    
- Suporte aos métodos **IMsgStore** que são específicos para o spooler MAPI: [IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)e [IMsgStore::](imsgstore-setlockstate.md)setlockstate.
    
O **** método setlockstate é importante para a interoperação adequada entre os clientes e o spooler MAPI. Quando o spooler MAPI chama setLockstate em uma mensagem de saída, o provedor do repositório de mensagens não deve permitir que os clientes Abram a mensagem. **** Se um cliente tentar abrir uma mensagem bloqueada pelo spooler MAPI, o provedor de repositório de mensagens deverá retornar MAPI_E_NO_ACCESS. O estado bloqueado de uma mensagem não precisa ser persistente, caso o repositório seja desligado enquanto a mensagem é bloqueada pelo spooler MAPI. 
  
Independentemente de o spooler MAPI ter bloqueado uma mensagem de saída, o provedor do repositório de mensagens não deve permitir que uma mensagem na fila de mensagens de saída seja aberta para gravação. Se um cliente chamar o método [IMSgStore:: OpenEntry](imsgstore-openentry.md) em uma mensagem de saída com o sinalizador MAPI_MODIFY, a chamada deverá falhar e retornar MAPI_E_SUBMITTED. Se um aplicativo cliente chama **OpenEntry** em uma mensagem de saída com o sinalizador MAPI_BEST_ACCESS, o provedor do repositório de mensagens deve permitir acesso somente leitura à mensagem. 
  
Quando uma mensagem é manipulada pelo spooler MAPI, o provedor do repositório de mensagens define a propriedade **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) da mensagem como SUBMITFLAG_LOCKED. O valor SUBMITFLAG_LOCKED indica que o spooler MAPI bloqueou a mensagem para seu uso exclusivo. O outro valor para **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, é definido quando a mensagem requer o pré-processamento por uma ou mais funções de pré-processador registradas por um provedor de transporte.
  
Os procedimentos a seguir descrevem como o repositório de mensagens, o transporte e o spooler MAPI interagem para enviar uma mensagem de um cliente para um ou mais destinatários. 
  
O aplicativo cliente chama o método [IMessage:: SubmitMessage](imessage-submitmessage.md) . No **SubmitMessage**, o provedor de armazenamento de mensagens faz o seguinte:
  
1. Chama [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md). Se MAPI retornar um erro, o provedor de armazenamento de mensagens retornará esse erro ao cliente.
    
2. Define o bit MSGFLAG_SUBMIT na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
    
3. Garante que exista uma coluna para a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) na tabela de destinatários e a defina como false para indicar que nenhum transporte ainda assumiu a responsabilidade de transmitir a mensagem.
    
4. Define a data e a hora da origem na propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Chama [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) para fazer o seguinte: 
    
    1. Expanda todas as listas de distribuição pessoal e destinatários personalizados e substitua todos os nomes de exibição alterados por seus nomes originais.
        
    2. Remover nomes duplicados.
        
    3. Verifique se há um pré-processamento necessário e, se o pré-processamento for necessário, defina o sinalizador NEEDS_PREPROCESSING e a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), que é reservada para MAPI. 
        
    4. Defina o sinalizador NEEDS_SPOOLER se o repositório de mensagens estiver rigidamente acoplado a um transporte e não puder lidar com todos os destinatários. 
    
6. Executa as seguintes tarefas se o sinalizador de mensagem NEEDS_PREPROCESSING estiver definido:
    
    1. Coloca a mensagem na fila de saída com o conjunto de bits SUBMITFLAG_PREPROCESS na propriedade **PR_SUBMIT_FLAGS** . 
        
    2. Notifica o spooler MAPI de que a fila foi alterada.
        
    3. Retorna o controle ao cliente e o fluxo de mensagens continua no spooler MAPI. O spooler MAPI realiza as seguintes tarefas: 
    
       1. Bloqueia a mensagem chamando [IMsgStore::](imsgstore-setlockstate.md)setlockstate.
            
       2. Realiza o pré-processamento necessário chamando todas as funções de pré-processamento na ordem de registro. Os provedores de transporte chamam [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar funções de pré-processamento. 
            
       3. Chama [IMessage:: SubmitMessage](imessage-submitmessage.md) na mensagem aberta para indicar ao repositório de mensagens que o pré-processamento está completo. 
    
Se não houver pré-processamento ou se houver pré-processamento e o spooler MAPI chamado **SubmitMessage**, o provedor de armazenamento de mensagens fará o seguinte no processo de cliente: 
  
- Realiza as seguintes tarefas se o repositório de mensagens estiver rigidamente acoplado a um transporte e o sinalizador NEEDS_SPOOLER retornado de [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md):
    
   - Cuida de qualquer destinatário que possa lidar.
    
   - Define a propriedade **PR_RESPONSIBILITY** como true para todos os destinatários que ele manipula. 
    
   - Realiza as seguintes tarefas se todos os destinatários forem conhecidos por esse transporte e transporte rigidamente acoplados: 
    
     - Chama [IMAPISupport:: CompleteMsg](imapisupport-completemsg.md) se a mensagem tiver sido preprocessada ou se o provedor de repositório de mensagens quiser que o spooler MAPI Complete o processamento de mensagens. O fluxo de mensagens continua com o spooler MAPI. 
    
     - Realiza as seguintes tarefas se a mensagem não tiver sido preprocessada ou se o provedor do repositório de mensagens não quiser que o spooler MAPI Complete o processamento de mensagens:
    
       1. Copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se definida.
            
       2. Exclui a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como true.
            
       3. Desbloqueia a mensagem se estiver bloqueada.
            
       4. Retorna ao cliente. O fluxo de mensagens foi concluído.
    
  - Executa as seguintes tarefas se a mensagem foi preprocessada ou o provedor quer que o spooler MAPI conclua o processamento de mensagens:
    
    1. Chama [IMAPISupport:: CompleteMsg](imapisupport-completemsg.md). 
          
    2. Continua o fluxo de mensagens com o spooler MAPI. Para obter mais informações, consulte [enviando mensagens: tarefas do spooler MAPI](sending-messages-mapi-spooler-tasks.md).
    
  - Executa as seguintes tarefas se a mensagem não foi preprocessada ou o provedor não deseja que o spooler conclua o processamento de mensagens:
    
    1. Copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** , se definida. 
        
    2. Exclui a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** tiver sido definida como true. 
        
    3. Desbloqueia a mensagem se estiver bloqueada. 
        
    4. Retorna ao chamador. O fluxo de mensagens foi concluído.
    
- Realiza as seguintes tarefas se o repositório de mensagens não estiver rigidamente acoplado a um transporte, nem todos os destinatários foram conhecidos no repositório de mensagens ou se o sinalizador NEEDS_SPOOLER estiver definido:
    
  1. Coloca a mensagem na fila de saída sem definir o bit SUBMITFLAG_PREPROCESS na propriedade **PR_SUBMIT_FLAGS** . 
    
  2. Notifica o spooler MAPI de que a fila de saída foi alterada gerando uma notificação de tabela. 
    
  3. Retorna ao cliente e o fluxo de mensagens continua com um conjunto de tarefas executadas pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também

- [Recursos do repositório de mensagens](message-store-features.md)

