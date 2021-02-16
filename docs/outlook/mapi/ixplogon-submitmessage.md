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
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423318"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que o spooler MAPI tem uma mensagem para o provedor de transporte entregar.
  
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
  
> [in] Uma máscara de bits de sinalizadores que controla como a mensagem é enviada. O sinalizador a seguir pode ser definido:
    
BEGIN_DEFERRED 
  
> O spooler MAPI está chamando um provedor de transporte com uma mensagem que foi adiada anteriormente. O identificador de entrada da mensagem é o mesmo de quando ela foi adiada. A mensagem foi adiada passando seu identificador de entrada de volta para o spooler MAPI usando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED usuário. 
    
 _lpMessage_
  
> [in] Um ponteiro para um objeto de mensagem (representando a mensagem a ser entregue) que tem permissão de leitura/gravação, que o provedor de transporte usa para acessar e manipular essa mensagem. Esse objeto permanece válido até que o provedor de transporte retorne de uma chamada subsequente para o [método IXPLogon::EndMessage.](ixplogon-endmessage.md) 
    
 _lpulMsgRef_
  
> [out] Um ponteiro para uma variável na qual o provedor de transporte retorna o valor de referência atribuído a essa mensagem. O spooler MAPI passa esse valor de referência em chamadas subsequentes para esta mensagem. O spooler MAPI inicializa o valor como 0 antes de retorá-lo para o provedor de transporte.
    
 _lpulReturnParm_
  
> [out] Um ponteiro para uma variável que corresponde ao valor MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR de erro retornado por **SubmitMessage**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BUSY 
  
> O provedor de transporte não pode manipular a mensagem, pois está executando outra operação. Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o spooler MAPI não deve chamar **EndMessage**. O spooler MAPI tentará a **chamada SubmitMessage** novamente mais tarde. 
    
MAPI_E_CANCEL 
  
> Embora o provedor de transporte tenha solicitado que o spooler MAPI resubmita a mensagem em uma chamada **SpoolerNotify** anterior, as condições foram alteradas desde então e a mensagem não deve ser reemitida. O spooler MAPI passará a tratar de outra coisa. 
    
MAPI_E_NETWORK_ERROR 
  
> Um erro de rede impede a conclusão bem-sucedida da operação. O  _parâmetro lpulReturnParm_ deve ser definido como o número de segundos que passará antes que o spooler MAPI resubmita a mensagem. 
    
MAPI_E_NOT_ME 
  
> O provedor de transporte não pode lidar com essa mensagem. O spooler MAPI deve tentar encontrar outro provedor de transporte para ele. Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o spooler MAPI não deve chamar **EndMessage**.
    
MAPI_E_WAIT 
  
> Um problema temporário impede que o provedor de transporte manipular a mensagem. O  _parâmetro lpulReturnParm_ deve ser definido como o número de segundos que passará antes que o spooler MAPI resubmita a mensagem. 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon::SubmitMessage** quando ele tem uma mensagem para o provedor de transporte entregar. A mensagem é passada para o provedor de transporte usando o _parâmetro lpMessage._ 
  
Se o provedor estiver pronto para aceitar a mensagem, ele deverá retornar um valor de referência usando o parâmetro  _lpulMsgRef,_ processar o objeto passado e retornar o valor apropriado (geralmente S_OK). Se o provedor não estiver preparado para lidar com a transferência, ele deverá retornar um valor de erro e, opcionalmente, outro valor de retorno MAPI em  _lpulReturnParm_ para indicar quanto tempo o spooler MAPI deve aguardar antes de reemitir a mensagem. 
  
A implementação desse método por um provedor de transporte pode fazer o seguinte:
  
- Coloque a mensagem em uma fila interna para aguardar a transmissão, possivelmente copiando a mensagem para o armazenamento local e retorne.
    
- Tente executar a transmissão real e retornar quando a transmissão for concluída, com êxito ou sem êxito.
    
- Determine se a mensagem será enviada após a verificação do recurso envolvido. Nesse caso, se o recurso estiver livre, o provedor poderá bloquear o recurso, preparar a mensagem e encaminhá-la. Se o recurso estiver ocupado, o provedor poderá preparar a mensagem e adiar o envio para uma hora posterior.
    
A técnica preferida para transmissão de mensagens depende do provedor de transporte e do número esperado de processos que competem por recursos do sistema. 
  
Durante uma **chamada SubmitMessage,** o provedor de transporte controla a transferência de dados de mensagem do objeto de mensagem. No entanto, o provedor de transporte deve atribuir um valor de referência à mensagem, ao qual retorna um ponteiro em  _lpulMsgRef_, antes de transferir dados. Isso acontece porque, a qualquer momento durante o processo, o spooler MAPI pode chamar o método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) com o sinalizador NOTIFY_CANCEL_MESSAGE definido para sinalizar ao provedor que ele deve liberar todos os objetos abertos e interromper a transferência de mensagens. 
  
O provedor de transporte não deve enviar nenhuma propriedade nãotransmitível da mensagem. Quando encontrar essa propriedade, ela deverá processar a próxima propriedade. O provedor deve se esforçar para não exibir MAPI_P1 de destinatário como parte do conteúdo da mensagem transmitida; o provedor deve usar essas informações de destinatário somente para fins de endereçamento. MAPI_P1 destinatários são destinatários gerados internamente que são usados para reending messages; eles não devem ser transmitidos. Em vez disso, use os outros destinatários para transmitir informações do destinatário. O objetivo dessa disposição é permitir que destinatários reend vejam exatamente a mesma tabela de destinatários que os destinatários originais.
  
Durante uma **chamada SubmitMessage,** o spooler MAPI processa métodos para objetos que são abertos durante a transferência da mensagem e processa todos os anexos. Esse processamento pode levar muito tempo. Os provedores de transporte podem chamar o método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o spooler MAPI frequentemente durante esse processamento para liberar tempo de CPU para outras tarefas do sistema. 
  
Todos os destinatários da mensagem ficam visíveis na tabela de destinatários da mensagem que o spooler MAPI originalmente passou. O provedor de transporte deve processar apenas os destinatários que ele pode manipular — com base no identificador de entrada, tipo de endereço ou ambos — e que ainda não têm sua propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como TRUE. Se **PR_RESPONSIBILITY** já estiver definido como TRUE, outro provedor de transporte terá tratado esse destinatário. Quando o provedor concluir o processamento suficiente de um destinatário para determinar se ele pode manipular mensagens para esse destinatário, ele deve definir a propriedade **PR_RESPONSIBILITY** desse destinatário como TRUE na mensagem passada. Normalmente, o provedor faz essa determinação após a conclusão da entrega da mensagem. 
  
Normalmente, o provedor de transporte não retorna de uma **chamada SubmitMessage** até concluir a transferência de dados da mensagem. Se nenhum erro for retornado, a próxima chamada do spooler MAPI para o provedor será uma chamada para o método [IXPLogon::EndMessage.](ixplogon-endmessage.md) 
  
Se **SubmitMessage retornar** um erro, o spooler MAPI liberará a mensagem em processo sem salvar as alterações. Se o provedor de transporte exigir que as alterações de mensagem sejam salvas, ele deverá chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem antes de retornar. 
  
Em caso de erros que ocorrem devido a problemas de transporte, o spooler MAPI retém a mensagem, mas atrasa a resubmissão da mensagem para o provedor de transporte com base no valor retornado em  _lpulReturnParm_. O provedor de transporte deverá preencher esse valor se o valor de retorno de **SubmitMessage** for MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR. Se ocorrer uma condição de erro grave, o provedor de transporte deverá chamar o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_CRITICAL_ERROR usuário. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

