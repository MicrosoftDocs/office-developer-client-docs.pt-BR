---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428855"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Sinaliza a ocorrência de um evento sobre o qual o provedor de transporte solicitou a notificação.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in, out] Uma bitmask de sinalizadores que sinaliza eventos de notificação. Os seguintes sinalizadores podem ser definidos pelo spooler MAPI na entrada e devem ser retornados inalterados na saída:
    
NOTIFY_ABORT_DEFERRED 
  
> Notifica o provedor de transporte de que uma mensagem para a qual aceitou a responsabilidade está sendo adiada. Somente os provedores de transporte que dão suporte ao adiamento devem oferecer suporte a esse sinalizador. O parâmetro _lppvData_ aponta para o identificador de entrada da mensagem cancelada. As mensagens que o spooler MAPI não tiver processado ainda poderão ser adiadas chamando o método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> O MAPI spooler pode agora aceitar mensagens de entrada para esta sessão do provedor de transporte. O spooler MAPI chama regularmente o método [IXPLogon::P oll](ixplogon-poll.md) se o provedor de transporte definir o sinalizador LOGON_SP_POLL com a chamada [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) no logon. Depois que o sinalizador NOTIFY_BEGIN_INBOUND estiver definido, o spooler MAPI honrará o sinalizador NOTIFY_NEWMAIL passado na chamada para o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . A linha da tabela de status da sessão do provedor de transporte deve ser atualizada antes de retornar chamando o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . Os sinalizadores NOTIFY_BEGIN_INBOUND e NOTIFY_END_INBOUND são mutuamente exclusivos. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Assinala o provedor de transporte para percorrer mensagens de entrada o mais rápido possível. Para atender a essa notificação, o provedor de transporte deve definir o sinalizador STATUS_INBOUND_FLUSH na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da linha da tabela de status, assim que possível, usando o **ModifyStatusRow**. Um ciclo de mensagens de entrada é concluído quando o provedor determina que ele tenha baixado tudo o que pode ou quando recebeu uma chamada de método **TransportNotify** com o sinalizador NOTIFY_END_INBOUND_FLUSH definido. Até o final do ciclo de mensagens de entrada, o provedor não deve chamar o método [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) ou ceder ciclos para o sistema operacional para acelerar a entrega de mensagens de entrada. Isso é aceitável porque o spooler MAPI normalmente usa o NOTIFY_BEGIN_INBOUND_FLUSH somente em resposta a uma solicitação do usuário, por meio de um aplicativo cliente, para entregar todas as mensagens agora. No final da operação de liberação de entrada, o provedor deve usar **SpoolerNotify** para limpar o sinalizador STATUS_INBOUND_FLUSH na propriedade **PR_STATUS_CODE** da linha de status. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> As operações de saída agora podem ocorrer para esta sessão do provedor de transporte. Se houver qualquer mensagem a ser enviada para esse provedor, uma chamada para o método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) segue. A linha da tabela de status desta sessão deve ser atualizada antes de retornar. Os sinalizadores NOTIFY_BEGIN_OUTBOUND e NOTIFY_END_OUTBOUND são mutuamente exclusivos. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funciona de forma semelhante ao sinalizador NOTIFY_BEGIN_INBOUND_FLUSH, mas se refere a mensagens de saída. O sinalizador de status apropriado é STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> O spooler MAPI deve cancelar a transferência da mensagem para a qual o parâmetro _lppvData_ aponta para o valor 32-bit da chamada do método **IXPLogon:: SubmitMessage** . O sinalizador NOTIFY_CANCEL_MESSAGE pode ser definido sem o provedor de transporte ter retornado da chamada do método **SubmitMessage**, **IXPLogon:: StartMessage**ou **IXPLogon:: endmessage** que está associada à mensagem. O provedor de transporte deve retornar o mais cedo possível do ponto de entrada que está tratando da mensagem cancelada. Para uma mensagem de entrada que está sendo processada no momento, o provedor de transporte deve salvar a mensagem de entrada onde estiver armazenada e fornecê-la novamente no próximo momento conveniente. Os dados do objeto Message já armazenados para a mensagem de entrada são descartados. Se o provedor de transporte não atualizar esse valor de 32 bits no horário **StartMessage** ou **SubmitMessage** , o valor será 0 para mensagens de saída e 1 para mensagens de entrada. 
    
NOTIFY_END_INBOUND 
  
> As operações de entrada devem cessar para esta sessão do provedor de transporte. O spooler MAPI deixa de usar o método **Poll** e ignora o NOTIFY_NEWMAIL para esta sessão. As mensagens em andamento devem ser concluídas. A linha da tabela de status da sessão de transporte deve ser atualizada chamando [ModifyStatusRow](imapisupport-modifystatusrow.md) antes de retornar. Os sinalizadores NOTIFY_END_INBOUND e NOTIFY_BEGIN_INBOUND são mutuamente exclusivos. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Notifica o provedor de transporte para sair do modo de liberação de entrada. O provedor de transporte não deve interromper o download, mas o download deve ser feito em segundo plano. A linha da tabela de status da sessão de transporte deve ser atualizada chamando **ModifyStatusRow** quando o provedor de transporte puder ser compatível com esta notificação. 
    
NOTIFY_END_OUTBOUND 
  
> As operações de saída devem cessar para esta sessão do provedor de transporte. O spooler MAPI deixa de chamar **SubmitMessage** e ignora o sinalizador **SpoolerNotify** NOTIFY_READYTOSEND. Se houver uma mensagem de saída sendo enviada, ela não deverá ser interrompida; para interromper a entrega de uma mensagem, use o sinalizador NOTIFY_CANCEL_MESSAGE. A linha da tabela de status desta sessão deve ser atualizada chamando **ModifyStatusRow** antes de retornar. Os sinalizadores NOTIFY_END_INBOUND e NOTIFY_BEGIN_OUTBOUND são mutuamente exclusivos. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funciona de forma semelhante a NOTIFY_END_INBOUND_FLUSH, mas se refere a mensagens de saída. O sinalizador de status apropriado é STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> bota Um ponteiro para um ponteiro para dados específicos de eventos. Para obter mais informações sobre o que o _lppvData_ especifica, consulte a descrição para o parâmetro _lpulFlags_ . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: TransportNotify** para sinalizar o provedor de transporte sobre eventos para os quais a notificação foi solicitada. Esses eventos incluem uma solicitação de spooler MAPI para cancelar uma transferência de mensagem, o início ou fim de operações de transporte de entrada ou saída e o início ou fim de uma operação para limpar uma fila de mensagens de entrada ou de saída. 
  
Quando o usuário tenta cancelar uma mensagem que o provedor de transporte tenha sido adiado anteriormente, o spooler MAPI chama **TransportNotify**, passando os sinalizadores NOTIFY_ABORT_DEFERRED e NOTIFY_CANCEL_MESSAGE no _parâmetroulflags_. Se o spooler MAPI estiver fazendo logoff e ainda tiver mensagens na fila, ele passará apenas NOTIFY_ABORT_DEFERRED no _parâmetroulflags_ quando chamar **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O provedor deve sincronizar o acesso aos seus dados nessa chamada, pois o spooler MAPI pode invocar esse método de outro thread de execução ou de um procedimento para uma janela diferente. Isso provavelmente ocorrerá quando o spooler MAPI sinalizar o cancelamento de uma mensagem de que o provedor de transporte começou a enviar.
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

