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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5429f98a0335ae99b719d0f15b66a95ba87430e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767758"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Aplica-se a**: Outlook 
  
Sinaliza a ocorrência de um evento sobre quais o provedor de transporte solicitado notificação.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Par�metros

 _lpulFlags_
  
> [além, out] Uma bitmask dos sinalizadores que sinaliza eventos de notificação. Sinalizadores a seguir podem ser definidos pelo MAPI spooler na entrada e devem ser retornados inalterados na saída:
    
NOTIFY_ABORT_DEFERRED 
  
> Notifica o provedor de transporte que uma mensagem para a qual ela aceita a responsabilidade está sendo adiada. Apenas os provedores de transporte que suportam adiamento devem oferecer suporte a esse sinalizador. O parâmetro _lppvData_ aponta para o identificador de entrada da mensagem cancelada. Mensagens que não processado o MAPI spooler ainda podem ser adiadas chamando o método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> O MAPI spooler agora pode aceitar mensagens de entrada para esta sessão de provedor de transporte. O MAPI spooler regularmente chama o método de [IXPLogon::Poll](ixplogon-poll.md) se o provedor de transporte definir o sinalizador LOGON_SP_POLL com a chamada [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) no logon. Depois que o sinalizador NOTIFY_BEGIN_INBOUND estiver definido, o MAPI spooler respeita o sinalizador NOTIFY_NEWMAIL passado na chamada para o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . A linha da tabela de status para a sessão do provedor de transporte deve ser atualizada antes de retornar chamando o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Os sinalizadores NOTIFY_BEGIN_INBOUND e NOTIFY_END_INBOUND são mutuamente exclusivos. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Sinaliza o provedor de transporte para percorrer mensagens de entrada mais depressa possível. Para cumprir essa notificação, o provedor de transporte deve definir o sinalizador STATUS_INBOUND_FLUSH na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da sua linha da tabela de status, assim que possível, usando **ModifyStatusRow**. Um ciclo de mensagens de entrada é concluído quando o provedor determina que ele tenha baixado todos puder ou quando ele recebeu uma chamada de método de **TransportNotify** com o sinalizador NOTIFY_END_INBOUND_FLUSH definido. Até o fim do ciclo de mensagens de entrada, o provedor não deve chamar o método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) ou caso contrário, ceder ciclos para o sistema operacional para entrega de velocidade de mensagens de entrada. Isso é aceitável como o spooler MAPI normalmente usa NOTIFY_BEGIN_INBOUND_FLUSH apenas em resposta a uma solicitação do usuário, por meio de um aplicativo cliente, para entregar todas as mensagens agora. No final da operação de liberação de entrada, o provedor deve usar o **SpoolerNotify** para limpar o sinalizador STATUS_INBOUND_FLUSH na propriedade **PR_STATUS_CODE** da sua linha de status. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Operações de saída podem ocorrer agora para esta sessão de provedor de transporte. Se houver todas as mensagens sejam enviadas para esse provedor, segue uma chamada ao método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . A linha da tabela de status para esta sessão deve ser atualizada antes de retornar. Os sinalizadores NOTIFY_BEGIN_OUTBOUND e NOTIFY_END_OUTBOUND são mutuamente exclusivos. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funciona de modo semelhante ao sinalizador NOTIFY_BEGIN_INBOUND_FLUSH, mas se refere às mensagens de saída. O sinalizador de status apropriado é STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> O MAPI spooler deve cancelar a transferência da mensagem para os quais os pontos de parâmetro _lppvData_ com o valor de 32 bits do método **IXPLogon::SubmitMessage** chamada. O sinalizador NOTIFY_CANCEL_MESSAGE pode ser definido sem o provedor de transporte tendo retornado do **SubmitMessage**, **IXPLogon::StartMessage**ou chamada de método **IXPLogon::EndMessage** que está associada com a mensagem. O provedor de transporte deve retornar assim que possível, do ponto de entrada que está tratando a mensagem cancelada. Para uma mensagem de entrada que está sendo processada, o provedor de transporte deve salvar a mensagem de entrada, onde quer que ele está armazenado no momento e entregá-lo novamente no próximo horário conveniente. Os dados do objeto de mensagem já armazenados para a mensagem de entrada são descartados. Se o provedor de transporte não foi atualizada para este valor de 32 bits no momento **StartMessage** ou **SubmitMessage** , o valor é 0 para mensagens de saída e 1 para mensagens de entrada. 
    
NOTIFY_END_INBOUND 
  
> Operações de entrada devem deixarão de existir para esta sessão de provedor de transporte. O MAPI spooler deixa de usar o método de **votação** e ignora NOTIFY_NEWMAIL para esta sessão. Mensagens em processo devem ser concluídas. A linha da tabela de status para a sessão de transporte deve ser atualizada chamando [ModifyStatusRow](imapisupport-modifystatusrow.md) antes de retornar. Os sinalizadores NOTIFY_END_INBOUND e NOTIFY_BEGIN_INBOUND são mutuamente exclusivos. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Notifica o provedor de transporte devem sair do modo de liberação de entrada. O provedor de transporte não deve parar o download, mas baixando deve ser feita em segundo plano. A linha da tabela de status para a sessão de transporte deve ser atualizada chamando **ModifyStatusRow** quando o provedor de transporte pode estar em conformidade com essa notificação. 
    
NOTIFY_END_OUTBOUND 
  
> Operações de saída devem deixarão de existir para esta sessão de provedor de transporte. O MAPI spooler deixa de chamada **SubmitMessage** e ignora o sinalizador NOTIFY_READYTOSEND **SpoolerNotify** . Se houver uma mensagem de saída sendo enviada atualmente, não deve ser interrompido; Para interromper a entrega de uma mensagem, use o sinalizador NOTIFY_CANCEL_MESSAGE. A linha da tabela de status para esta sessão deve ser atualizada chamando **ModifyStatusRow** antes de retornar. Os sinalizadores NOTIFY_END_INBOUND e NOTIFY_BEGIN_OUTBOUND são mutuamente exclusivos. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funciona da mesma forma para NOTIFY_END_INBOUND_FLUSH, mas se refere às mensagens de saída. O sinalizador de status apropriado é STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Um ponteiro para um ponteiro para dados de eventos específicos. Para obter mais informações sobre quais _lppvData_ Especifica, consulte a descrição para o parâmetro _lpulFlags_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

O MAPI spooler chama o método de **IXPLogon::TransportNotify** para sinalizar o provedor de transporte sobre eventos de notificação para o qual tiver sido solicitada. Esses eventos incluem uma solicitação de spooler MAPI para cancelar uma transferência de mensagem, o início ou final das operações de transporte de entrada ou de saída e início ou no fim de uma operação para limpar uma fila de mensagens de entrada ou de saída. 
  
Quando o usuário tenta cancelar uma mensagem que o provedor de transporte foi adiada anteriormente, o MAPI spooler chama **TransportNotify**, passando sinalizadores NOTIFY_ABORT_DEFERRED tanto o NOTIFY_CANCEL_MESSAGE em _ulFlags_. Se o MAPI spooler é fazer logoff e ainda tem mensagens na fila, ele passa apenas NOTIFY_ABORT_DEFERRED em _ulFlags_ quando ele chama **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Notas para implementadores

O provedor deve sincronizar o acesso aos seus dados nessa chamada, pois o MAPI spooler pode chamar esse método a partir de outro thread de execução ou um procedimento para uma janela diferente. Isso provavelmente ocorrerá quando o MAPI spooler sinaliza o cancelamento de uma mensagem que o provedor de transporte foi iniciado enviando.
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon: IUnknown](ixplogoniunknown.md)

