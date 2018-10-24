---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575872"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que o MAPI spooler tem uma mensagem para o provedor de transporte fornecer.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a mensagem é enviada. O seguinte sinalizador pode ser definido:
    
BEGIN_DEFERRED 
  
> O MAPI spooler está chamando um provedor de transporte com uma mensagem que foi adiada anteriormente. O identificador de entrada da mensagem é o mesmo quando ele foi adiado. A mensagem foi adiada passando seu identificador de entrada volta para o MAPI spooler usando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> [in] Um ponteiro para um objeto de mensagem (representando a entrega da mensagem) que tem a permissão de leitura/gravação, que o provedor de transporte usa para acessar e manipular a mensagem. Este objeto permanecerá válido até depois que o provedor de transporte retorna de uma chamada subsequente ao método [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> [out] Um ponteiro para uma variável em que o provedor de transporte retornará o valor de referência atribuído a esta mensagem. O MAPI spooler passa esse valor de referência em chamadas subsequentes para esta mensagem. O MAPI spooler inicializa o valor como 0 antes de retorná-lo para o provedor de transporte.
    
 _lpulReturnParm_
  
> [out] Um ponteiro para uma variável que corresponde ao valor de erro MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR retornado por **SubmitMessage**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BUSY 
  
> O provedor de transporte não pode manipular a mensagem, porque ele está executando outra operação. Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o MAPI spooler não deve chamar **EndMessage**. O MAPI spooler tentará a chamada **SubmitMessage** novamente mais tarde. 
    
MAPI_E_CANCEL 
  
> Embora o provedor de transporte solicitado que o MAPI spooler reenviar a mensagem em uma chamada anterior de **SpoolerNotify** , condições alterou e não deve ser reenviada a mensagem. O MAPI spooler irão lidar com algo diferente. 
    
MAPI_E_NETWORK_ERROR 
  
> Um erro de rede impediu a conclusão bem-sucedida da operação. O parâmetro _lpulReturnParm_ deve ser definido como o número de segundos que decorrerá antes que o MAPI spooler reenvia a mensagem. 
    
MAPI_E_NOT_ME 
  
> O provedor de transporte não pode manipular esta mensagem. O MAPI spooler deve tentar localizar o outro provedor de transporte para ele. Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o MAPI spooler não deve chamar **EndMessage**.
    
MAPI_E_WAIT 
  
> Um problema temporário impede que o provedor de transporte tratamento da mensagem. O parâmetro _lpulReturnParm_ deve ser definido como o número de segundos que decorrerá antes que o MAPI spooler reenvia a mensagem. 
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método de **IXPLogon::SubmitMessage** quando ele tem uma mensagem para o provedor de transporte fornecer. A mensagem será passada para o provedor de transporte usando o parâmetro _lpMessage_ . 
  
Se o provedor está pronto para aceitar a mensagem, ela deve retornar um valor de referência usando o parâmetro _lpulMsgRef_ , o objeto passado, de processo e retornar o valor apropriado (geralmente S_OK). Se o provedor não está preparado para lidar com a transferência, ele deverá retornar um valor de erro e, opcionalmente, MAPI outro valor de retorno no _lpulReturnParm_ para indicar quanto tempo o MAPI spooler deve aguardar antes de reenviar a mensagem. 
  
Implementação de um provedor de transporte deste método pode fazer o seguinte:
  
- Colocar a mensagem em uma fila interna para aguardar a transmissão, possivelmente copiar a mensagem para o armazenamento local e retornar.
    
- Tente executar a transmissão real e retornar quando a transmissão for concluído com sucesso ou não.
    
- Determine se deseja enviar a mensagem após a verificação do recurso envolvidos. Nesse caso, se o recurso estiver disponível, o provedor pode bloquear o recurso, preparar a mensagem e enviá-la. Se o recurso estiver ocupado, o provedor pode preparar a mensagem e adiar enviando para um momento posterior.
    
A técnica preferida para transmissão de mensagens depende do provedor de transporte e o número esperado de processos competindo por recursos do sistema. 
  
Durante uma chamada de **SubmitMessage** , o provedor de transporte controla a transferência de dados de mensagem do objeto de mensagem. No entanto, o provedor de transporte deve atribuir um valor de referência para a mensagem, ao qual ele retorna um ponteiro em _lpulMsgRef_, antes de transferir os dados. Ele então porque a qualquer momento durante o processo, o MAPI spooler pode chamar o método de [IXPLogon::TransportNotify](ixplogon-transportnotify.md) com o sinalizador NOTIFY_CANCEL_MESSAGE definido para sinalizar o provedor que deve liberar todos os objetos e interromper a transferência de mensagem. 
  
O provedor de transporte não deve enviar todas as propriedades nontransmittable da mensagem. Quando encontrar uma propriedade inexistente, ele deverá ir para processar a propriedade next. O provedor deve fazer todos os esforços para não exibir informações do destinatário MAPI_P1 como parte do conteúdo da mensagem transmitida; o provedor deve usar essas informações de destinatário apenas para fins de endereçamento. Destinatários de MAPI_P1 são gerados internamente destinatários que são usados para reenviar mensagens; eles não devem ser transmitidos. Em vez disso, use os outros destinatários para transmitir informações do destinatário. A finalidade dessa organização é permitir que os destinatários de reenvio para ver a tabela de destinatários mesma exata como os destinatários originais.
  
Durante uma chamada de **SubmitMessage** , o MAPI spooler processa os métodos de objetos que estão abertos durante a transferência da mensagem e processa todos os anexos. Esse processamento pode levar muito tempo. Provedores de transporte podem chamar o método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o MAPI spooler frequentemente durante o processamento para liberar o tempo da CPU para outras tarefas do sistema. 
  
Todos os destinatários da mensagem são visíveis na tabela de destinatário da mensagem que o MAPI spooler originalmente passado. O provedor de transporte deve processar somente os destinatários que pode manipular — com base no tipo de endereço, o identificador de entrada ou ambos — e que ainda não tem sua propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como TRUE. Se **PR_RESPONSIBILITY** já estiver definida como TRUE, a outro provedor de transporte manipulou que o destinatário. Quando o provedor conclui o processamento suficiente de um destinatário para determinar se ele pode lidar com as mensagens para que o destinatário, ele deve definir a propriedade **PR_RESPONSIBILITY** de que o do destinatário como TRUE na mensagem passada. Geralmente, o provedor torna essa determinação após a conclusão da entrega da mensagem. 
  
Normalmente, o provedor de transporte não retorna de uma chamada de **SubmitMessage** até que ele seja concluída a transferência de dados de mensagem. Se nenhum erro será retornado, a próxima chamada do spooler MAPI para o provedor é uma chamada ao método [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
  
Se **SubmitMessage** retornará um erro, o MAPI spooler libera a mensagem no processo sem salvar as alterações. Se o provedor de transporte requer alterações de mensagem a ser salvo, ele deve chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem de antes retornando. 
  
Em caso de erros que ocorrem devido a problemas de transporte, o MAPI spooler mantém a mensagem, mas ele atrasa reenviar a mensagem para o provedor de transporte com base no valor retornado no _lpulReturnParm_. O provedor de transporte deve preencher esse valor se o seu valor de retorno de **SubmitMessage** é MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR. Se ocorrer uma condição de erro grave, o provedor de transporte deve chamar o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_CRITICAL_ERROR. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

