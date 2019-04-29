---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423766"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o spooler MAPI sobre uma alteração no status ou uma solicitação de serviço. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que indica o tipo de notificação. Os provedores de transporte podem definir todos os sinalizadores, exceto NOTIFY_NEWMAIL_RECEIVED; somente NOTIFY_NEWMAIL_RECEIVED e NOTIFY_READTOSEND são válidos para provedores de repositórios de mensagens. Os seguintes sinalizadores são válidos para o parâmetro _parâmetroulflags_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Registra uma solicitação para alterar a configuração do provedor de transporte. 
    
NOTIFY_CRITICAL_ERROR 
  
> Ocorreu um erro irrecuperável no provedor de transporte. Como NOTIFY_SENTDEFERRED e NOTIFY_CRITICAL_ERROR usam o parâmetro _lpvData_ para chamadas de provedor de transporte, esses sinalizadores são mutuamente exclusivos. 
    
NOTIFY_CRITSEC 
  
> Solicita uma seção crítica para o provedor de transporte. O parâmetro _lpvData_ está indefinido e deve ser nulo. 
    
NOTIFY_NEWMAIL 
  
> O spooler MAPI deve baixar mensagens recebidas recentemente no próximo horário disponível. O parâmetro _lpvData_ está indefinido e deve ser definido como nulo. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Uma nova mensagem foi recebida no repositório de mensagens. O parâmetro _lpvData_ aponta para uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que descreve a mensagem. Esse sinalizador é usado para provedores de repositório de mensagens que estão rigidamente acoplados a provedores de transporte e é ignorado se o provedor de repositório estiver conectado com o sinalizador MAPI_NO_MAIL definido. 
    
NOTIFY_NONCRIT 
  
> Libera uma seção crítica obtida com uma chamada anterior para **SpoolerNotify** com _PARÂMETROULFLAGS_ definido como NOTIFY_CRITSEC. O parâmetro _lpvData_ está indefinido e deve ser definido como nulo. 
    
NOTIFY_READYTOSEND 
  
> O provedor de armazenamento de mensagens ou de transporte está pronto para enviar mensagens. O parâmetro _lpvData_ está indefinido e deve ser definido como nulo. 
    
NOTIFY_SENTDEFERRED 
  
> Uma mensagem adiada anteriormente deve ser enviada agora e o provedor de transporte deve ser notificado quando a mensagem estiver pronta para ser entregue usando uma chamada para o método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) . O identificador de entrada da mensagem adiada está contido em uma estrutura [SBinary](sbinary.md) indicada por _lpvData_. Como tanto NOTIFY_SENTDEFERRED quanto NOTIFY_CRITICAL_ERROR usam o parâmetro _lpvData_ , esses sinalizadores são mutuamente exclusivos. 
    
 _lpvData_
  
> no Um ponteiro para dados associados aplicáveis a uma notificação. O parâmetro _lpvData_ aponta para dados válidos somente quando os seguintes sinalizadores são definidos (_lpvData_ é nulo quando _parâmetroulflags_ é definido como os outros tipos de notificação): 
    
|**configuração _parâmetroulflags_**|**valor _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informações sobre o erro.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Uma estrutura **NEWMAIL_NOTIFICATION** que contém informações sobre a mensagem recentemente entregue.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Uma estrutura **SBinary** que contém o identificador de entrada da mensagem adiada.  <br/> |
   
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: SpoolerNotify** é implementado para os objetos de repositório de mensagens e de suporte do provedor de transporte. Esses provedores chamam **SpoolerNotify** para notificar o spooler MAPI sobre uma alteração no status ou uma solicitação de serviço. **SpoolerNotify** é chamado principalmente por provedores de transporte e pode ser chamado a qualquer momento durante a sessão. 
  
## <a name="notes-to-transport-providers"></a>Observações para provedores de transporte

Se você tiver alterado a configuração do provedor de transporte, chame **SpoolerNotify** e defina _parâmetroulflags_ como NOTIFY_CONFIG_CHANGED. **SpoolerNotify** responde chamando o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para consultar uma alteração nos tipos de endereço com suporte. 
  
Se você precisar de uma seção crítica para garantir o processamento sem interrupção, chame **SpoolerNotify** com _PARÂMETROULFLAGS_ definido como NOTIFY_CRITSEC. A definição desse sinalizador informa ao spooler MAPI que ele não deve chamar os métodos [IXPLogon:: Idle](ixplogon-idle.md) e [IXPLogon::P oll](ixplogon-poll.md) . Embora você tenha uma seção crítica aberta, retorne MAPI_E_BUSY sempre que o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) for chamado. Ao concluir a seção crítica, faça outra chamada para **SpoolerNotify** com _PARÂMETROULFLAGS_ definido como NOTIFY_NONCRIT. 
  
Por exemplo, se o seu provedor de transporte remoto estiver no processo de carregamento de mensagens, talvez seja necessário permitir que um usuário insira um número de telefone para estabelecer a conexão remota. Antes de executar um loop no procedimento da caixa de diálogo, você deve declarar uma seção crítica. Quando o usuário fechar a caixa de diálogo, terminando o procedimento da caixa de diálogo, você deverá liberar a seção crítica.
  
Quando você define _parâmetroulflags_ como NOTIFY_CRITICAL_ERROR, o spooler MAPI não faz mais chamadas para o provedor, exceto para liberá-lo. Se você chamar **SpoolerNotify** com NOTIFY_CRITICAL_ERROR definido dos métodos [IXPLogon:: StartMessage](ixplogon-startmessage.md) ou [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) , retorne com um valor de erro apropriado da chamada **StartMessage** ou * * SubmitMessage * * imediatamente após a chamada **SpoolerNotify** . 
  
Se o seu provedor de transporte for recuperado de uma condição que anteriormente causou a falha, chame **SpoolerNotify** com _PARÂMETROULFLAGS_ definido como NOTIFY_READYTOSEND. Esse sinalizador indica que o provedor está pronto novamente para lidar com as mensagens. 
  
## <a name="notes-to-message-store-providers"></a>Observações para provedores de repositórios de mensagens

Chame **SpoolerNotify**, passando o sinalizador NOTIFY_READYTOSEND no _parâmetroulflags_, antes de fazer sua primeira chamada para [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) no **IMessage:: SubmitMessage**. Essa chamada para **SpoolerNotify** precisa ser feita apenas uma vez por sessão. 
  
Se o seu provedor de repositório de mensagens estiver rigidamente acoplado a um provedor de transporte e você chamar **SpoolerNotify** com _PARÂMETROULFLAGS_ definido como NOTIFY_NEWMAIL_RECEIVED, o spooler MAPI abrirá a nova mensagem e começará a processar a nova função de gancho de mensagem. Quando o processamento estiver concluído, o spooler MAPI chama o método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para informá-lo sobre sua própria mensagem nova. 
  
Para obter mais informações sobre como chamar o **SpoolerNotify**, consulte qualquer um dos seguintes tópicos:
  
- [Implementar o método FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interagir com o spooler MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modelo de recebimento de mensagens](message-reception-model.md)
    
## <a name="see-also"></a>Confira também



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

