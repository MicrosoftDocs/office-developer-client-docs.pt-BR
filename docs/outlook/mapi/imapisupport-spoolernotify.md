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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767287"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Aplica-se a**: Outlook 
  
Notifica o MAPI spooler de uma alteração no status ou uma solicitação de serviço. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que indica o tipo de notificação. Provedores de transporte podem definir todos os sinalizadores, exceto NOTIFY_NEWMAIL_RECEIVED; apenas NOTIFY_NEWMAIL_RECEIVED e NOTIFY_READTOSEND são válidos para provedores de armazenamento de mensagem. Sinalizadores a seguir são válidos para o parâmetro _ulFlags_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Registra uma solicitação para alterar a configuração do provedor de transporte. 
    
NOTIFY_CRITICAL_ERROR 
  
> Um erro irreparável ocorreu para o provedor de transporte. Como NOTIFY_SENTDEFERRED e o NOTIFY_CRITICAL_ERROR usam o parâmetro _lpvData_ para chamadas de provedor de transporte, esses sinalizadores são mutuamente exclusivos. 
    
NOTIFY_CRITSEC 
  
> Solicita uma seção crítica para o provedor de transporte. O parâmetro _lpvData_ é indefinido e deve ser nula. 
    
NOTIFY_NEWMAIL 
  
> O MAPI spooler deve baixar quaisquer mensagens recebidas recentemente no próximo horário disponível. O parâmetro _lpvData_ é indefinido e deve ser definido como NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Uma nova mensagem foi recebida no repositório de mensagem. O parâmetro _lpvData_ aponta para uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que descreve a mensagem. Esse sinalizador é usado para provedores de armazenamento de mensagem que estejam intimamente ligadas a provedores de transporte e é ignorada se o provedor de repositório está conectado com o sinalizador MAPI_NO_MAIL definido. 
    
NOTIFY_NONCRIT 
  
> Libera uma seção crítica que foi obtida com uma chamada anterior a **SpoolerNotify** com _ulFlags_ definido como NOTIFY_CRITSEC. O parâmetro _lpvData_ é indefinido e deve ser definido como NULL. 
    
NOTIFY_READYTOSEND 
  
> O provedor de repositórios de transporte ou de mensagem está pronto para enviar mensagens. O parâmetro _lpvData_ é indefinido e deve ser definido como NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Uma mensagem adiada anteriormente agora deve ser enviada e o provedor de transporte deve ser notificado quando a mensagem está pronta para ser entregues por meio de uma chamada ao método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . O identificador de entrada da mensagem adiada está contido em uma estrutura de [SBinary](sbinary.md) apontada pela _lpvData_. Como NOTIFY_SENTDEFERRED e o NOTIFY_CRITICAL_ERROR usam o parâmetro _lpvData_ , esses sinalizadores são mutuamente exclusivos. 
    
 _lpvData_
  
> [in] Um ponteiro para os dados associados aplicáveis a uma notificação. O parâmetro _lpvData_ aponta para dados válido somente quando os seguintes sinalizadores estão definidos (_lpvData_ é NULL quando _ulFlags_ estiver definido como os outros tipos de notificação): 
    
|**configuração de _ulFlags_**|**valor de _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informações sobre o erro.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Uma estrutura **NEWMAIL_NOTIFICATION** que contém informações sobre a mensagem entregue recentemente.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Uma estrutura de **SBinary** que contém o identificador de entrada de mensagem adiada.  <br/> |
   
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::SpoolerNotify** é implementado para mensagem armazenar e objetos de suporte do provedor de transporte. Esses provedores chamarem **SpoolerNotify** para notificar o MAPI spooler de uma alteração no status ou uma solicitação de serviço. **SpoolerNotify** é chamado principalmente pelos provedores de transporte e pode ser chamado a qualquer momento durante a sessão. 
  
## <a name="notes-to-transport-providers"></a>Observações para provedores de transporte

Se você tiver alterado sua configuração de provedor de transporte, chame **SpoolerNotify** e defina _ulFlags_ como NOTIFY_CONFIG_CHANGED. **SpoolerNotify** responde chamando o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) a consulta para uma alteração de tipos de endereço com suporte. 
  
Se você precisar de uma seção crítica para garantir o processamento ininterrupto, chame **SpoolerNotify** com _ulFlags_ definido como NOTIFY_CRITSEC. Defina esse sinalizador informa o MAPI spooler que ele não deve chamar os métodos [IXPLogon::Idle](ixplogon-idle.md) e [IXPLogon::Poll](ixplogon-poll.md) . Enquanto uma seção crítica aberto, retorne MAPI_E_BUSY sempre que o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) é chamado. Quando você terminar com a seção crítica, fazer outra chamada para **SpoolerNotify** com _ulFlags_ definido como NOTIFY_NONCRIT. 
  
Por exemplo, se seu provedor de transporte remoto estiver no processo de carregamento de mensagens, você precisará permitir que o usuário insira um número de telefone para estabelecer a conexão remota. Antes de você percorrer o procedimento da caixa de diálogo, você deve declarar uma seção crítica. Quando o usuário fechar a caixa de diálogo, encerrando o procedimento da caixa de diálogo, você deve liberar a seção crítica.
  
Quando você definir _ulFlags_ como NOTIFY_CRITICAL_ERROR, o spooler MAPI não faz nenhuma chamada adicional para o provedor, exceto ao liberá-la. Se você chamar **SpoolerNotify** com NOTIFY_CRITICAL_ERROR definir a partir dos métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , retornar com um valor de erro apropriado do **StartMessage** ou * * SubmitMessage * * chamada imediatamente após a chamada **SpoolerNotify** . 
  
Se o seu provedor de transporte recuperados de uma condição que anteriormente deixá-lo falhar, chame **SpoolerNotify** com _ulFlags_ definido como NOTIFY_READYTOSEND. Esse sinalizador indica que o provedor está pronto para lidar com as mensagens novamente. 
  
## <a name="notes-to-message-store-providers"></a>Observações para provedores de armazenamento de mensagens

Chame **SpoolerNotify**, passando o sinalizador NOTIFY_READYTOSEND _ulFlags_, antes de fazer a chamada primeira para [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) no **IMessage::SubmitMessage**. Essa chamada para **SpoolerNotify** deve ser feita apenas uma vez por sessão. 
  
Se o seu provedor de armazenamento de mensagem está intimamente ligado com um transporte provedor e você chamar **SpoolerNotify** com _ulFlags_ definido para NOTIFY_NEWMAIL_RECEIVED, o MAPI spooler abre a nova mensagem e inicia o processamento a nova função de gancho de mensagem. Quando o processamento estiver concluído, o MAPI spooler chama o método de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informar sua própria mensagem nova. 
  
Para obter mais informações sobre como chamar **SpoolerNotify**, consulte qualquer um dos seguintes tópicos:
  
- [Implementando o método FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interação com o Spooler MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modelo de recepção de mensagem](message-reception-model.md)
    
## <a name="see-also"></a>Confira também



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

