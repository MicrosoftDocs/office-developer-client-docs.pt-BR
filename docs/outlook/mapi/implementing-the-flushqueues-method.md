---
title: Implementando o método FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: baafd8b6437f4febaee9420b274c20ba3242cae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767455"
---
# <a name="implementing-the-flushqueues-method"></a>Implementando o método FlushQueues

  
  
**Aplica-se a**: Outlook 
  
O MAPI spooler usa o método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) para baixar e carregar qualquer mensagens pendentes de e para um provedor de transporte. Normalmente, o MAPI spooler irá liberar as filas para todos os provedores de transporte que esteja conectados à sessão, começando com o primeiro provedor de transporte, conforme definido na seção de ordem de transporte do perfil do usuário. Filas de liberar quase sempre é o resultado de uma solicitação direta pelo usuário, o envio e recebimento de mensagens enquanto as filas são liberação são síncrona para o spooler MAPI. Como essas chamadas são síncronas, o provedor de transporte deve processá-los assim que possível. 
  
Provedores de transporte devem lidar com a chamada **FlushQueues** conforme descrito na seguinte sequência de etapas para habilitar o processamento da mensagem adequadas e habilitar recursos externos como modems a ser usado por outros provedores de transporte, como parte do spooler MAPI Operação **FlushQueues** . 
  
|**Etapa**|**Componente**|**Implementação**|
|:-----|:-----|:-----|
|1.  <br/> |Spooler MAPI  <br/> |Chama o método **FlushQueues** para o primeiro provedor de transporte listado na ordem de transporte do perfil do usuário, passando os sinalizadores solicitados no parâmetro _ulFlags_ . **FlushQueues** é chamado de uma vez com todos os sinalizadores definido para o carregamento inteiro e a operação de download.  <br/> |
|2.  <br/> |Provedor de transporte  <br/> |Você precisa fazer um número de itens antes de retornar da chamada **FlushQueues** . Se enviados anteriormente mensagens estão sendo adiadas, o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) deve ser chamado com o sinalizador NOTIFY_SENT_DEFERRED definido. Observe que é possível que o spooler MAPI cancelar uma mensagem que foi adiada antes do provedor de transporte tem uma chance para concluir o processamento da mensagem.  <br/> Se o provedor de transporte usa um recurso externo, como um modem, a conexão para o recurso externo deve ser estabelecida.  <br/> O STATUS_OUTBOUND_FLUSH bit na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da linha de status do provedor de transporte deve ser definida usando o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) .  <br/> O provedor de transporte, em seguida, deve retornar S_OK para a chamada **FlushQueues** .  <br/> |
|3.  <br/> |Spooler MAPI  <br/> |Verifica a linha de status do provedor de transporte para o bit STATUS_OUTBOUND_FLUSH e chama [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) para a primeira mensagem na fila.  <br/> |
|4.  <br/> |Provedor de transporte  <br/> |Manipula a mensagem e retorna da chamada **SubmitMessage** .  <br/> |
|5.  <br/> |Spooler MAPI  <br/> |Se o provedor de transporte Retorna S_OK de **SubmitMessage**, o MAPI spooler chama [IXPLogon::EndMessage](ixplogon-endmessage.md) para a mensagem como acontece com o envio de mensagem normal.  <br/> Se o provedor de transporte retorna um valor que não seja S_OK de **SubmitMessage**, o MAPI spooler manipula o valor apropriadamente, antes de chamar **EndMessage**ou antes de chamar **SubmitMessage** novamente.  <br/> |
|6.  <br/> |Provedor de transporte  <br/> |Retorna a partir **EndMessage** com seu status no parâmetro _lpulFlags_ de processamento de mensagens.  <br/> |
|7.  <br/> |Provedor de transporte e o spooler MAPI  <br/> |O **SubmitMessage**- **EndMessage** loop continua até que todas as mensagens na fila foram baixadas.  <br/> |
|8.  <br/> |Spooler MAPI  <br/> |Notifica o provedor de transporte que foi finalizada baixando mensagens chamando o método de [IXPLogon::TransportNotify](ixplogon-transportnotify.md) de transporte do provedor com o sinalizador NOTIFY_END_OUTBOUND_FLUSH definido.  <br/> |
|9.  <br/> |Provedor de transporte  <br/> |Libera quaisquer recursos externos usados no envio de mensagens de saída para que eles possam ser usados por outros provedores de transporte para liberar suas filas.  <br/> O STATUS_INBOUND_FLUSH bit na propriedade **PR_STATUS_CODE** da linha de status do provedor de transporte deve ser definida usando **ModifyStatusRow**.  <br/> |
|10.  <br/> |Spooler MAPI  <br/> |Verifica a linha de status do provedor de transporte para o bit STATUS_INBOUND_FLUSH e chama [IXPLogon::StartMessage](ixplogon-startmessage.md) se ele estiver definido.  <br/> |
|11.  <br/> |Provedor de transporte  <br/> |Processa a mensagem e retorna a partir de **StartMessage**. Se o provedor de transporte tem outras mensagens para carregar, ele deve chamar **SpoolerNotify** com o sinalizador NOTIFY_NEWMAIL definido.  <br/> Se o provedor de transporte não tiver nenhuma mensagem para carregar, ele deve chamar [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem o MAPI spooler passadas em **StartMessage** e retornar.  <br/> |
|12.  <br/> |Spooler MAPI  <br/> |Continua a chamar **StartMessage** até **SaveChanges** for chamado em uma mensagem. Depois que o provedor de transporte concluiu o carregamento, o MAPI spooler chama **TransportNotify** com o sinalizador NOTIFY_END_INBOUND_FLUSH definido.  <br/> |
|13.  <br/> |Provedor de transporte  <br/> |Limpa o STATUS_INBOUND_FLUSH bit na propriedade **PR_STATUS_CODE** da sua linha de status usando **ModifyStatusRow** e versões de todos os recursos externos para que estejam disponíveis para usarem por outros provedores de transporte.  <br/> |
|14.  <br/> |Spooler MAPI  <br/> |Chama **FlushQueues** para o provedor de transporte próximo listado na ordem de transporte do perfil do usuário.  <br/> |
   
Se a chamadas do aplicativo de cliente [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) no objeto de status de um provedor de transporte, o provedor de transporte deve definir o bit apropriado em sua linha de status com **ModifyStatusRow**. O MAPI spooler, em seguida, chama o método de **IXPLogon::FlushQueues** do provedor de transporte em conveniência do spooler MAPI. Quando método de **IXPLogon::FlushQueues** do provedor de transporte é chamado como resultado de uma chamada de **IMAPIStatus::FlushQueues** de um aplicativo cliente, a operação assíncrona ocorre ao aplicativo cliente. Caso contrário, **IXPLogon::FlushQueues** funciona de maneira síncrona com o spooler MAPI. 
  
Por motivos de desempenho, o MAPI spooler apenas chamará método **FlushQueues** de um provedor de transporte se os sinalizadores STATUS_INBOUND_FLUSH e STATUS_OUTBOUND_FLUSH são definidos na linha de status do provedor de transporte. Consequentemente, um provedor de transporte pode interromper a operação de **FlushQueues** a qualquer momento, desmarcando os sinalizadores STATUS_OUTBOUND_FLUSH e STATUS_INBOUND_FLUSH em sua linha de status. Se o MAPI spooler está sendo desligado e precisa finalizar a operação de **FlushQueues** , ele chama **TransportNotify** com o conjunto de sinalizadores de NOTIFY_END_INBOUND_FLUSH e NOTIFY_END_OUTBOUND_FLUSH. O provedor de transporte deve liberar todos os recursos externos e retornar. 
  

