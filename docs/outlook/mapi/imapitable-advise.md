---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418810"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um objeto sink de aviso para receber notificação de eventos especificados que afetam a tabela.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulEventMask_
  
> [in] Valor que indica o tipo de evento que gerará a notificação. Somente o seguinte valor é válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Ponteiro para um objeto sink de aviso para receber as notificações subsequentes. Esse objeto sink de aconselhmento já deve ter sido alocado.
    
 _lpulConnection_
  
> [out] Ponteiro para um valor que não seja zero que representa o registro de notificação bem-sucedido.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi concluído com êxito.
    
MAPI_E_NO_SUPPORT 
  
> A implementação da tabela não dá suporte a alterações em suas linhas e colunas ou não dá suporte à notificação.
    
## <a name="remarks"></a>Comentários

Use o **método IMAPITable::Advise** para registrar um objeto de tabela implementado no provedor para retornos de chamada de notificação. Sempre que ocorre uma alteração no objeto table, o provedor verifica qual bit da máscara de eventos foi definido no parâmetro  _ulEventMask_ e, portanto, qual tipo de alteração ocorreu. Se um bit for definido, o provedor chamará o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto sink advise indicado pelo parâmetro  _lpAdviseSink_ para relatar o evento. Os dados passados na estrutura de notificação para a **rotina OnNotify** descrevem o evento. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou a qualquer momento seguinte. Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer thread. Para uma maneira de transformar uma chamada para **OnNotify** que pode acontecer em um momento inoportuno em um que seja mais seguro de manipular, um provedor deve usar a função [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Para fornecer notificações, o provedor que implementa **o Advise** precisa manter uma cópia do ponteiro para o objeto sink de _aviso lpAdviseSink;_ para fazer isso, ele chama o método **IUnknown::AddRef** para o sink de aviso manter seu ponteiro de objeto até que o registro de notificação seja cancelado com uma chamada para o método [IMAPITable::Unadvise.](imapitable-unadvise.md) A **implementação de** Aviso deve atribuir um número de conexão ao registro de notificação e chamar **AddRef** nesse número de conexão antes de reenvolvê-lo no parâmetro _lpulConnection._ Os provedores de serviços podem liberar o objeto sink de avisar antes que o registro seja cancelado, mas eles não devem liberar o número de conexão até que ** Unadvise ** tenha sido chamado. 
  
Depois que uma chamada para **o Advise** tiver sido bem-sucedida e antes de ** Unadvise ** ter sido chamado, os clientes devem estar preparados para que o objeto de cliente aconselhado seja liberado. Um cliente deve, portanto, liberar seu objeto de cliente de aconselhá-lo após o retorno de **Advise,** a menos que tenha um uso específico a longo prazo para ele. 
  
Devido ao comportamento assíncrono da notificação, implementações que alteram as configurações de coluna da tabela podem receber notificações com informações organizadas em uma ordem de coluna anterior. Por exemplo, uma linha de tabela pode ser retornada para uma mensagem que acabou de ser excluída do contêiner. Essa notificação é enviada quando a alteração na configuração da coluna é feita e as informações sobre ela são enviadas, mas a exibição da tabela de notificação ainda não foi atualizada com essas informações.
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter informações específicas sobre a notificação de tabela, consulte [Sobre notificações de tabela.](about-table-notifications.md) Para obter informações sobre como usar os **métodos IMAPISupport** para dar suporte à notificação, consulte [Notificação de Evento de Suporte.](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI usa o **método IMAPITable::Advise** para registrar notificações para permitir que o modo de exibição de tabela permaneça atualizado.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

