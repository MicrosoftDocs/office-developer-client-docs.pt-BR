---
title: Provedores de armazenamento de envio de mensagens por meio de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: aaba816ca7efab6cee939087a18332561f31b81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770357"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Provedores de armazenamento de envio de mensagens por meio de mensagem

**Aplica-se a**: Outlook 
  
Provedores de armazenamento de mensagens não são necessárias para dar suporte a envios de mensagem de saída (ou seja, a capacidade para aplicativos de cliente para usar o provedor de armazenamento de mensagem para enviar mensagens). Aplicativos cliente precisam usar um armazenamento de mensagens, enquanto o envio de mensagens, pois os dados da mensagem devem ser armazenados em algum lugar entre o momento em que o usuário está concluído redigi-lo e a hora em que o MAPI spooler fornece a mensagem a um provedor de transporte para envio para o sistema de mensagens subjacente. Se o seu provedor de armazenamento de mensagens não oferece suporte a envios de mensagem de saída, ele não pode ser usado como o armazenamento de mensagens padrão.
  
Para suportar o envio de mensagens, seu provedor de armazenamento de mensagem deve fazer o seguinte:
  
- Implemente uma fila de mensagens de saída.
    
- Suporte ao método [IMessage::SubmitMessage](imessage-submitmessage.md) em objetos de mensagem criados no repositório de mensagem. 
    
- Oferece suporte a métodos **IMsgStore** que são específica para o spooler MAPI: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)e [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
O método **SetLockState** é importante para adequadas interoperação entre o spooler MAPI e clientes. Quando o MAPI spooler ligar **SetLockState** em uma mensagem de saída, o provedor de armazenamento de mensagem deve não permitir que clientes abra a mensagem. Se um cliente tentar abrir uma mensagem que está bloqueada pelo spooler MAPI, o provedor de armazenamento de mensagem deve retornar MAPI_E_NO_ACCESS. O estado bloqueado de uma mensagem não precisam ser persistente caso o repositório for desligado enquanto a mensagem está bloqueada pelo spooler MAPI. 
  
Independentemente se o MAPI spooler bloqueou uma mensagem de saída, o provedor de armazenamento de mensagem não deve permitir uma mensagem na fila de mensagens de saída para ser aberto para gravação. Se um cliente chama o método [IMSgStore::OpenEntry](imsgstore-openentry.md) em uma mensagem de saída com o sinalizador MAPI_MODIFY, a chamada deve falhar e retornar MAPI_E_SUBMITTED. Se um aplicativo cliente chama **OpenEntry** em uma mensagem de saída com o sinalizador MAPI_BEST_ACCESS, o provedor de armazenamento de mensagem deve permitir acesso somente leitura à mensagem. 
  
Quando uma mensagem é sejam manipuladas pelo MAPI spooler, o provedor de armazenamento de mensagem define a propriedade de **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) da mensagem para SUBMITFLAG_LOCKED. O valor SUBMITFLAG_LOCKED indica que o MAPI spooler tiver bloqueado a mensagem para seu uso exclusivo. O outro valor para **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, é definido quando a mensagem requer a pré-processamento por uma ou mais funções pré-processador registradas por um provedor de transporte.
  
Os procedimentos a seguir descrevem como o armazenamento de mensagens, transporte e spooler MAPI interagem para enviar uma mensagem de um cliente para um ou mais destinatários. 
  
O aplicativo cliente chama o método [IMessage::SubmitMessage](imessage-submitmessage.md) . Em **SubmitMessage**, o provedor de armazenamento de mensagem faz o seguinte:
  
1. Chama [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). Se o MAPI retornará um erro, o provedor de armazenamento de mensagem retorna esse erro ao cliente.
    
2. Define o MSGFLAG_SUBMIT bit na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
    
3. Garante que existe uma coluna para a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) na tabela de destinatário e define como FALSE para indicar que nenhum transporte ainda tem assumido responsabilidade para transmitir a mensagem.
    
4. Define a data e hora de origem na propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Chamadas [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) para fazer o seguinte: 
    
    1. Expandir todas as listas de distribuição pessoal e destinatários personalizados e substitua todos os nomes de exibição alterados por seus nomes originais.
        
    2. Remova nomes duplicados.
        
    3. Verifique qualquer pré-processamento necessário e, se for necessário pré-processamento, defina o sinalizador NEEDS_PREPROCESSING e a propriedade **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), que é reservada para MAPI. 
        
    4. Defina o sinalizador NEEDS_SPOOLER se o armazenamento de mensagens está firmemente combinado com um transporte e ele não pode lidar com todos os destinatários. 
    
6. Se o sinalizador de mensagem NEEDS_PREPROCESSING estiver definido, executa as seguintes tarefas:
    
    1. Coloca a mensagem na fila de saída com o bit SUBMITFLAG_PREPROCESS definido na propriedade **PR_SUBMIT_FLAGS** . 
        
    2. Notifica o spooler MAPI que a fila foi alterada.
        
    3. Retorna o controle para o cliente e o fluxo de mensagens continua no spooler MAPI. O MAPI spooler executa as seguintes tarefas: 
    
       1. Bloqueia a mensagem chamando [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Executa o needed pré-processamento chamando todas as funções pré-processamento na ordem de registro. Provedores de transporte chamarem [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar as funções de pré-processamento. 
            
       3. [IMessage::SubmitMessage](imessage-submitmessage.md) na mensagem aberta para indicar à mensagem armazenar esse pré-processamento de chamadas está concluída. 
    
Não se houve nenhum pré-processamento ou houve pré-processamento e o spooler MAPI chamado **SubmitMessage**, o provedor de armazenamento de mensagem faz o seguinte no processo de cliente: 
  
- Se o armazenamento de mensagens está intimamente ligado a um transporte e o sinalizador NEEDS_SPOOLER foi retornado de [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md), executa as seguintes tarefas:
    
   - Trata quaisquer destinatários que pode manipular.
    
   - Define a propriedade **PR_RESPONSIBILITY** como TRUE para quaisquer destinatários que ele manipula. 
    
   - Se todos os destinatários são conhecidos como esse ligação estreita de armazenamento e o transporte, executa as seguintes tarefas: 
    
     - Chama [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) se a mensagem foi pré-processado ou o spooler MAPI para processamento de mensagens completas quer que o provedor de armazenamento de mensagem. Fluxo de mensagens continua com o spooler MAPI. 
    
     - Se a mensagem não foi pré-processado ou o provedor de armazenamento de mensagem não deseja que o spooler MAPI para concluir o processamento de mensagens, executa as seguintes tarefas:
    
       1. Copia a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), se definida.
            
       2. Exclui a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) tiver sido definida como TRUE.
            
       3. Desbloqueia a mensagem se ele estiver bloqueado.
            
       4. Retorna para o cliente. Fluxo de mensagens é concluído.
    
  - Se a mensagem foi pré-processado ou o provedor quer o MAPI spooler para concluir o processamento de mensagens, executa as seguintes tarefas:
    
    1. Chama [IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Continua o fluxo de mensagens com o spooler MAPI. Para obter mais informações, consulte [enviando mensagens: tarefas de Spooler MAPI](sending-messages-mapi-spooler-tasks.md).
    
  - Se a mensagem não foi pré-processado ou o provedor não deseja que o spooler para concluir o processamento de mensagens, executa as seguintes tarefas:
    
    1. Cópias em que a mensagem para a pasta identificada pelo identificador de entrada na propriedade **PR_SENTMAIL_ENTRYID** , se definida. 
        
    2. Exclui a mensagem se a propriedade **PR_DELETE_AFTER_SUBMIT** tiver sido definida como TRUE. 
        
    3. Desbloqueia a mensagem se ele estiver bloqueado. 
        
    4. Retorna ao chamador. Fluxo de mensagens é concluído.
    
- Se o armazenamento de mensagens não está intimamente ligado a um transporte, nem todos os destinatários eram conhecidos para o armazenamento de mensagens ou o sinalizador NEEDS_SPOOLER estiver definido, executa as seguintes tarefas:
    
  1. Coloca a mensagem na fila de saída sem definir estará definido o bit SUBMITFLAG_PREPROCESS na propriedade **PR_SUBMIT_FLAGS** . 
    
  2. Notifica o spooler MAPI que a fila de saída foi alterada gerando uma notificação de tabela. 
    
  3. Continua a retorna para o cliente e o fluxo de mensagens com um conjunto de tarefas realizadas pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também

- [Recursos do repositório de mensagens](message-store-features.md)

