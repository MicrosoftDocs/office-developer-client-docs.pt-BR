---
title: Implementando o método FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411775"
---
# <a name="implementing-the-flushqueues-method"></a>Implementando o método FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O spooler MAPI usa o método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) para baixar e carregar mensagens pendentes de e para um provedor de transporte. Normalmente, o spooler MAPI liberará as filas para todos os provedores de transporte que estão conectados à sessão, começando com o primeiro provedor de transporte conforme definido na seção de ordem de transporte do perfil do usuário. A liberação de filas quase sempre é o resultado de uma solicitação direta do usuário, portanto, o envio e o recebimento de mensagens enquanto as filas estão sendo liberados é síncrono para o spooler MAPI. Como essas chamadas são síncronas, o provedor de transporte deve processá-las o mais rápido possível. 
  
Os provedores de transporte devem manipular a chamada **FlushQueues,** conforme descrito na sequência de etapas a seguir, para habilitar o processamento adequado de mensagens e permitir que recursos externos, como modems, sejam usados por outros provedores de transporte como parte da operação **FlushQueues** do spooler MAPI. 
  
|**Etapa**|**Componente**|**Implementação**|
|:-----|:-----|:-----|
|1.  <br/> |Spooler MAPI  <br/> |Chama o **método FlushQueues** para o primeiro provedor de transporte listado na ordem de transporte do perfil do usuário, passando os sinalizadores solicitados no _parâmetro ulFlags._ **FlushQueues é** chamado uma vez com todos os sinalizadores definidos para toda a operação de upload e download.  <br/> |
|2.  <br/> |Provedor de Transporte  <br/> |Precisa fazer várias coisas antes de retornar da **chamada FlushQueues.** Se as mensagens enviadas anteriormente estão sendo adiadas, o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) deve ser chamado com o sinalizador NOTIFY_SENT_DEFERRED definido. Observe que é possível que o spooler MAPI cancele uma mensagem que foi adiada antes que o provedor de transporte tenha a chance de concluir o processamento da mensagem.  <br/> Se o provedor de transporte usar um recurso externo, como um modem, a conexão com o recurso externo deverá ser estabelecida.  <br/> O STATUS_OUTBOUND_FLUSH bit na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da linha de status do provedor de transporte deve ser definido usando o método [IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md)  <br/> Em seguida, o provedor de transporte S_OK a **chamada FlushQueues.**  <br/> |
|3.  <br/> |Spooler MAPI  <br/> |Verifica a linha de status do provedor de transporte para STATUS_OUTBOUND_FLUSH bit e chama [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) para a primeira mensagem na fila.  <br/> |
|4.  <br/> |Provedor de transporte  <br/> |Lida com a mensagem e retorna da **chamada SubmitMessage.**  <br/> |
|5.  <br/> |Spooler MAPI  <br/> |Se o provedor de transporte retornar S_OK de **SubmitMessage**, o spooler MAPI chamará [IXPLogon::EndMessage](ixplogon-endmessage.md) para a mensagem da mesma forma que faz com o envio regular de mensagens.  <br/> Se o provedor de transporte retornar um valor diferente de S_OK de **SubmitMessage**, o spooler MAPI tratará o valor adequadamente antes de chamar **EndMessage** ou antes de chamar **SubmitMessage** novamente.  <br/> |
|6.  <br/> |Provedor de transporte  <br/> |Retorna de **EndMessage com** seu status de processamento de mensagens no parâmetro _lpulFlags._  <br/> |
|7.  <br/> |Provedor de transporte e spooler MAPI  <br/> |O loop **SubmitMessage** -  **EndMessage** continua até que todas as mensagens na fila tenham sido baixadas.  <br/> |
|8.  <br/> |Spooler MAPI  <br/> |Notifica o provedor de transporte de que terminou de baixar mensagens chamando o método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) do provedor de transporte com o sinalizador NOTIFY_END_OUTBOUND_FLUSH definido.  <br/> |
|9.  <br/> |Provedor de transporte  <br/> |Libera todos os recursos externos usados no envio de mensagens de saída para que possam ser usados por outros provedores de transporte para liberar suas filas.  <br/> O STATUS_INBOUND_FLUSH bit na **PR_STATUS_CODE** da linha de status do provedor de transporte deve ser definido usando **ModifyStatusRow**.  <br/> |
|10.  <br/> |Spooler MAPI  <br/> |Verifica a linha de status do provedor de transporte em busca STATUS_INBOUND_FLUSH bit e chama [IXPLogon::StartMessage](ixplogon-startmessage.md) se ele estiver definido.  <br/> |
|11.  <br/> |Provedor de transporte  <br/> |Processa a mensagem e retorna **de StartMessage**. Se o provedor de transporte tiver outras mensagens para carregar, ele deverá chamar **SpoolerNotify** com o sinalizador NOTIFY_NEWMAIL definido.  <br/> Se o provedor de transporte não tiver mensagens para carregar, ele deverá chamar [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem que o spooler MAPI passou em **StartMessage** e retornar.  <br/> |
|12.  <br/> |Spooler MAPI  <br/> |Continua chamando **StartMessage** até **SaveChanges** ser chamado em uma mensagem. Depois que o provedor de transporte terminar de carregar, o spooler MAPI **chamará TransportNotify** com o sinalizador NOTIFY_END_INBOUND_FLUSH definido.  <br/> |
|13.  <br/> |Provedor de transporte  <br/> |Limpa o STATUS_INBOUND_FLUSH bit na propriedade **PR_STATUS_CODE** de sua linha de status usando **ModifyStatusRow** e libera todos os recursos externos para que eles sejam disponibilizados para uso por outros provedores de transporte.  <br/> |
|14.  <br/> |Spooler MAPI  <br/> |Chama **FlushQueues** para o próximo provedor de transporte listado na ordem de transporte do perfil do usuário.  <br/> |
   
Se um aplicativo cliente chamar [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) no objeto de status de um provedor de transporte, o provedor de transporte deverá definir o bit apropriado em sua linha de status com **ModifyStatusRow**. Em seguida, o spooler MAPI chama o método **IXPLogon::FlushQueues** do provedor de transporte por conveniência do spooler MAPI. Quando o método **IXPLogon::FlushQueues** do provedor de transporte é chamado como resultado da chamada **IMAPIStatus::FlushQueues** de um aplicativo cliente, a operação ocorre de forma assíncrona para o aplicativo cliente. Caso **contrário, IXPLogon::FlushQueues** funciona de forma síncrona com o spooler MAPI. 
  
Por motivos de desempenho, o spooler MAPI chamará apenas o método **FlushQueues** de um provedor de transporte se os sinalizadores STATUS_INBOUND_FLUSH e STATUS_OUTBOUND_FLUSH são definidos na linha de status do provedor de transporte. Consequentemente, um provedor de transporte pode interromper a operação **FlushQueues** a qualquer momento limpando os sinalizadores STATUS_OUTBOUND_FLUSH e STATUS_INBOUND_FLUSH na linha de status. Se o spooler MAPI estiver sendo desligado e precisar finalizar a operação **FlushQueues,** ele chamará **TransportNotify** com os sinalizadores NOTIFY_END_INBOUND_FLUSH e NOTIFY_END_OUTBOUND_FLUSH definidos. O provedor de transporte deve liberar todos os recursos externos e retornar. 
  

