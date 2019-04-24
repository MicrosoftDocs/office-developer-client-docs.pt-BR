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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351587"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que o spooler MAPI tem uma mensagem para o provedor de transporte fornecer.
  
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
  
> no Uma bitmask de sinalizadores que controla como a mensagem é enviada. O seguinte sinalizador pode ser definido:
    
BEGIN_DEFERRED 
  
> O spooler MAPI está chamando um provedor de transporte com uma mensagem que foi adiada anteriormente. O identificador de entrada da mensagem é o mesmo que quando ela foi adiada. A mensagem foi adiada passando seu identificador de entrada de volta para o spooler MAPI usando o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> no Um ponteiro para um objeto Message (representando a mensagem a ser entregue) que tem permissão de leitura/gravação, que o provedor de transporte usa para acessar e manipular essa mensagem. Este objeto permanece válido até que o provedor de transporte retorne de uma chamada subsequente para o método [IXPLogon:: endmessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> bota Um ponteiro para uma variável na qual o provedor de transporte retorna o valor de referência atribuído a essa mensagem. O spooler MAPI passa esse valor de referência em chamadas subsequentes para esta mensagem. O spooler MAPI Inicializa o valor como 0 antes de devolvê-lo ao provedor de transporte.
    
 _lpulReturnParm_
  
> bota Um ponteiro para uma variável que corresponde ao valor de erro MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR retornado por **SubmitMessage**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BUSY 
  
> O provedor de transporte não pode lidar com a mensagem porque está executando outra operação. Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o spooler MAPI não deve chamar **endmessage**. O spooler MAPI tentará executar a chamada **SubmitMessage** novamente mais tarde. 
    
MAPI_E_CANCEL 
  
> Embora o provedor de transporte solicitou que o spooler MAPI reenvie a mensagem em uma chamada anterior do **SpoolerNotify** , as condições foram alteradas, e a mensagem não deve ser enviada novamente. O spooler MAPI será ativado para lidar com outra coisa. 
    
MAPI_E_NETWORK_ERROR 
  
> Um erro de rede impediu a conclusão bem-sucedida da operação. O parâmetro _lpulReturnParm_ deve ser definido como o número de segundos decorridos antes de o spooler MAPI reenviar a mensagem. 
    
MAPI_E_NOT_ME 
  
> O provedor de transporte não pode lidar com esta mensagem. O spooler MAPI deve tentar localizar outro provedor de transporte para ele. Um provedor deve usar esse valor de retorno para indicar que nenhum processamento ocorreu e que o spooler MAPI não deve chamar **endmessage**.
    
MAPI_E_WAIT 
  
> Um problema temporário impede que o provedor de transporte trate a mensagem. O parâmetro _lpulReturnParm_ deve ser definido como o número de segundos decorridos antes de o spooler MAPI reenviar a mensagem. 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: SubmitMessage** quando ele tem uma mensagem para que o provedor de transporte seja entregue. A mensagem é passada para o provedor de transporte usando o parâmetro _lpMessage_ . 
  
Se o provedor estiver pronto para aceitar a mensagem, ele deverá retornar um valor de referência usando o parâmetro _lpulMsgRef_ , processar o objeto passado e retornar o valor apropriado (geralmente S_OK). Se o provedor não estiver preparado para lidar com a transferência, ele deverá retornar um valor de erro e, opcionalmente, outro valor de retorno MAPI em _lpulReturnParm_ para indicar quanto tempo o spooler MAPI deve aguardar antes de reenviar a mensagem. 
  
A implementação de um provedor de transporte desse método pode fazer o seguinte:
  
- Coloque a mensagem em uma fila interna para aguardar a transmissão, possivelmente copiando a mensagem para o armazenamento local e retornar.
    
- Tente executar a transmissão real e retornar quando a transmissão for concluída, com êxito ou sem êxito.
    
- Determine se deseja enviar a mensagem após verificar o recurso envolvido. Nesse caso, se o recurso for gratuito, o provedor poderá bloquear o recurso, preparar a mensagem e enviá-la. Se o recurso estiver ocupado, o provedor poderá preparar a mensagem e adiar o envio para um momento posterior.
    
A técnica preferida para transmissão de mensagens depende do provedor de transporte e do número esperado de processos competindo por recursos do sistema. 
  
Durante uma chamada **SubmitMessage** , o provedor de transporte controla a transferência de dados de mensagem do objeto Message. No enTanto, o provedor de transporte deve atribuir um valor de referência à mensagem, para a qual ele retorna um ponteiro no _lpulMsgRef_, antes da transferência de dados. Ele faz isso porque em qualquer momento durante o processo, o spooler MAPI pode chamar o método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) com o sinalizador NOTIFY_CANCEL_MESSAGE definido para sinalizar ao provedor que ele deve liberar qualquer objeto aberto e interromper a transferência de mensagens. 
  
O provedor de transporte não deve enviar nenhuma propriedade não transmittable da mensagem. Quando encontra essa propriedade, ela deve ir para processar a próxima propriedade. O provedor deve fazer com que todos os esforços não exibam informações de destinatário do MAPI_P1 como parte do conteúdo da mensagem transmitida; o provedor deve usar essas informações de destinatário somente para fins de endereçamento. Os destinatários do MAPI_P1 são destinatários gerados internamente que são usados para reenviar mensagens; Eles não devem ser transmitidos. Em vez disso, use outros destinatários para transmitir informações do destinatário. A finalidade dessa organização é permitir que os destinatários reenviem para ver a mesma tabela de destinatários que os destinatários originais.
  
Durante uma chamada **SubmitMessage** , o spooler MAPI processa os métodos para objetos que são abertos durante a transferência da mensagem e processa todos os anexos. Esse processamento pode levar muito tempo. Os provedores de transporte podem chamar o método [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) para o spooler MAPI com frequência durante esse processamento para liberar o tempo de CPU para outras tarefas do sistema. 
  
Todos os destinatários da mensagem estão visíveis na tabela de destinatários da mensagem que o spooler MAPI originalmente aprovou. O provedor de transporte deve processar somente os destinatários que podem lidar com base no identificador de entrada, tipo de endereço ou ambos — e que ainda não têm sua propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) definida como true. Se **PR_RESPONSIBILITY** já estiver definido como true, outro provedor de transporte tratou esse destinatário. Quando o provedor concluir o processamento suficiente de um destinatário para determinar se ele pode lidar com mensagens desse destinatário, deverá definir a propriedade **PR_RESPONSIBILITY** desse destinatário como true na mensagem passada. Normalmente, o provedor faz essa determinação após a conclusão da entrega da mensagem. 
  
Normalmente, o provedor de transporte não retorna de uma chamada **SubmitMessage** até que conclua a transferência de dados da mensagem. Se nenhum erro for retornado, a próxima chamada do spooler MAPI ao provedor será uma chamada para o método [IXPLogon:: endmessage](ixplogon-endmessage.md) . 
  
Se **SubmitMessage** retornar um erro, o spooler MAPI libera a mensagem em processo sem salvar as alterações. Se o provedor de transporte exigir que as alterações de mensagem sejam salvas, ele deverá chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem antes de retornar. 
  
No caso de erros que ocorrem por causa de problemas de transporte, o spooler MAPI retém a mensagem, mas atrasa o reenvio da mensagem para o provedor de transporte com base no valor retornado em _lpulReturnParm_. O provedor de transporte deve preencher esse valor se o valor de retorno de **SubmitMessage** for MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR. Se ocorrer uma condição de erro grave, o provedor de transporte deverá chamar o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_CRITICAL_ERROR. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

