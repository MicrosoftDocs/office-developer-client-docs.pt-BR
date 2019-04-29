---
title: Implementar o método FlushQueues
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
# <a name="implementing-the-flushqueues-method"></a>Implementar o método FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI spooler usa o método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) para baixar e carregar todas as mensagens pendentes para e de um provedor de transporte. Normalmente, o spooler MAPI libera as filas para todos os provedores de transporte que estão conectados à sessão, começando com o primeiro provedor de transporte, conforme definido na seção ordem de transporte do perfil do usuário. A liberação de filas é quase sempre o resultado de uma solicitação direta pelo usuário, portanto, o envio e recebimento de mensagens enquanto as filas estão sendo liberadas são síncronos para o spooler MAPI. Como essas chamadas são síncronas, o provedor de transporte deve processá-las o mais rápido possível. 
  
Os provedores de transporte devem lidar com a chamada **FlushQueues** , conforme descrito na seguinte sequência de etapas para habilitar o processamento de mensagens apropriado e para habilitar recursos externos, como modems a serem usados por outros provedores de transporte como parte do MAPI spooler Operação **FlushQueues** . 
  
|**Etapa**|**Componente**|**Implementação**|
|:-----|:-----|:-----|
|1.  <br/> |Spooler MAPI  <br/> |Chama o método **FlushQueues** para o primeiro provedor de transporte listado na ordem de transporte do perfil do usuário, passando os sinalizadores solicitados no parâmetro _parâmetroulflags_ . **FlushQueues** é chamado uma vez com todos os sinalizadores definidos para a operação de upload e download inteira.  <br/> |
|2.  <br/> |Provedor de transporte  <br/> |O precisa fazer várias coisas antes de retornar da chamada **FlushQueues** . Se as mensagens enviadas anteriormente estiverem sendo adiadas, o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) deverá ser chamado com o sinalizador NOTIFY_SENT_DEFERRED definido. Observe que é possível que o spooler MAPI cancele uma mensagem que tenha sido adiada antes que o provedor de transporte tenha a chance de concluir o processamento da mensagem.  <br/> Se o provedor de transporte usar um recurso externo, como um modem, a conexão com o recurso externo deverá ser estabelecida.  <br/> O bit STATUS_OUTBOUND_FLUSH na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da linha de status do provedor de transporte deve ser definido usando o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) .  <br/> O provedor de transporte deve retornar S_OK para a chamada **FlushQueues** .  <br/> |
|3.  <br/> |Spooler MAPI  <br/> |Verifica a linha de status do provedor de transporte para o bit STATUS_OUTBOUND_FLUSH e chama [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) para a primeira mensagem na fila.  <br/> |
|4.  <br/> |Provedor de transporte  <br/> |Manipula a mensagem e retorna da chamada **SubmitMessage** .  <br/> |
|5.  <br/> |Spooler MAPI  <br/> |Se o provedor de transporte retornar S_OK de **SubmitMessage**, o spooler MAPI chamará [IXPLogon:: endmessage](ixplogon-endmessage.md) da mensagem como faz com o envio de mensagem regular.  <br/> Se o provedor de transporte retornar um valor diferente de S_OK de **SubmitMessage**, o spooler MAPI tratará o valor apropriadamente antes de chamar endmessage ou antes de chamar **SubmitMessage** novamente. ****  <br/> |
|6.  <br/> |Provedor de transporte  <br/> |Retorna de **endmessage** com seu status de processamento de mensagens no parâmetro _lpulFlags_ .  <br/> |
|7.  <br/> |Spooler MAPI e provedor de transporte  <br/> |O loop de endmessage do **SubmitMessage**- **** continua até que todas as mensagens na fila tenham sido baixadas.  <br/> |
|8.  <br/> |Spooler MAPI  <br/> |Notifica o provedor de transporte que concluiu o download de mensagens chamando o método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) do provedor de transporte com o sinalizador NOTIFY_END_OUTBOUND_FLUSH definido.  <br/> |
|9.  <br/> |Provedor de transporte  <br/> |Libera os recursos externos usados no envio de mensagens de saída para que eles possam ser usados por outros provedores de transporte para liberar suas filas.  <br/> O bit STATUS_INBOUND_FLUSH na propriedade **PR_STATUS_CODE** da linha de status do provedor de transporte deve ser definido usando o **ModifyStatusRow**.  <br/> |
|10.  <br/> |Spooler MAPI  <br/> |Verifica a linha de status do provedor de transporte para o bit STATUS_INBOUND_FLUSH e chama [IXPLogon:: StartMessage](ixplogon-startmessage.md) se estiver definido.  <br/> |
|11.  <br/> |Provedor de transporte  <br/> |Processa a mensagem e retorna de **StartMessage**. Se o provedor de transporte tiver outras mensagens para carregar, deverá chamar **SpoolerNotify** com o sinalizador NOTIFY_NEWMAIL definido.  <br/> Se o provedor de transporte não tiver mensagens para carregar, deverá chamar [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) na mensagem que o spooler MAPI aprovou no **StartMessage** e retornar.  <br/> |
|3,6.  <br/> |Spooler MAPI  <br/> |Continua chamando **StartMessage** até que **SaveChanges** seja chamado em uma mensagem. Após o provedor de transporte ter concluído o carregamento, o spooler MAPI chama **TransportNotify** com o sinalizador NOTIFY_END_INBOUND_FLUSH definido.  <br/> |
|Treze.  <br/> |Provedor de transporte  <br/> |Limpa o bit STATUS_INBOUND_FLUSH na propriedade **PR_STATUS_CODE** da linha de status usando **ModifyStatusRow** e libera todos os recursos externos para que fiquem disponíveis para uso por outros provedores de transporte.  <br/> |
|14.  <br/> |Spooler MAPI  <br/> |Chama **FlushQueues** para o próximo provedor de transporte listado na ordem de transporte do perfil do usuário.  <br/> |
   
Se um aplicativo cliente chama [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) em um objeto de status do provedor de transporte, o provedor de transporte deve definir o bit apropriado em sua linha de status com **ModifyStatusRow**. O spooler MAPI chama o método **IXPLogon:: FlushQueues** do provedor de transporte na conveniência do spooler do MAPI. Quando o método **IXPLogon:: FlushQueues** do provedor de transporte é chamado como resultado de uma chamada **IMAPIStatus:: FlushQueues** de um aplicativo cliente, a operação ocorre de forma assíncrona com o aplicativo cliente. Caso contrário, **IXPLogon:: FlushQueues** funciona de forma síncrona com o spooler MAPI. 
  
Por motivos de desempenho, o spooler MAPI só chamará o método **FlushQueues** de um provedor de transporte se os sinalizadores STATUS_INBOUND_FLUSH e STATUS_OUTBOUND_FLUSH estiverem definidos na linha de status do provedor de transporte. Consequentemente, um provedor de transporte pode parar a operação **FlushQueues** a qualquer momento, limpando os sinalizadores STATUS_OUTBOUND_FLUSH e STATUS_INBOUND_FLUSH em sua linha de status. Se o spooler MAPI estiver sendo desligado e precisar concluir a operação **FlushQueues** , ele chamará o **TransportNotify** com os sinalizadores NOTIFY_END_INBOUND_FLUSH e NOTIFY_END_OUTBOUND_FLUSH definidos. O provedor de transporte deve liberar todos os recursos externos e retornar. 
  

