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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329011"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um objeto de coletor de aviso para receber notificações de eventos especificados que afetam a tabela.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulEventMask_
  
> no O valor que indica o tipo de evento que gerará a notificação. Apenas o seguinte valor é válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> no Ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes. Este objeto de coletor de aviso deve já ter sido alocado.
    
 _lpulConnection_
  
> bota Ponteiro para um valor diferente de zero que representa o registro de notificação bem-sucedido.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi concluído com êxito.
    
MAPI_E_NO_SUPPORT 
  
> A implementação de tabela não oferece suporte a alterações em suas linhas e colunas ou não oferece suporte a notificações.
    
## <a name="remarks"></a>Comentários

Use o método imApitable **:: Advise** para registrar um objeto Table implementado no provedor para retornos de chamada de notificação. Sempre que uma alteração ocorre no objeto Table, o provedor verifica se o bit de máscara de evento foi definido no parâmetro _ulEventMask_ e, portanto, que tipo de alteração ocorreu. Se um bit for definido, o provedor chamará o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para o objeto de coletor de aviso indicado pelo parâmetro _lpAdviseSink_ para relatar o evento. Dados passados na estrutura de notificação para a **** rotina OnNotify descreve o evento. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou no momento seguinte. Em sistemas que oferecem suporte a vários threads de execução, **** a chamada para OnNotify pode ocorrer em qualquer thread. Para obter uma chamada para onNotificar **** que pode ocorrer em um horário do inopportune em um que seja mais seguro para lidar, um provedor deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para fornecer notificações, a **recomendação** de provedor de implementação precisa manter uma cópia do ponteiro para o objeto do coletor de aviso _lpAdviseSink_ ; para fazer isso, ele chama o método **IUnknown:: AddRef** para o coletor de avisos para manter seu ponteiro de objeto até que o registro de notificação seja cancelado com uma chamada para o método IMAPITable [:: Unadvise](imapitable-unadvise.md) . A implementação de **aviso** deve atribuir um número de conexão ao registro de notificação e chamar **AddRef** nesse número de conexão antes de devolvê-lo no parâmetro _lpulConnection_ . Os provedores de serviços podem liberar o objeto de coletor de aviso antes de o registro ser cancelado, mas não devem liberar o número de conexão até que * * Unadvise * * tenha sido chamado. 
  
Após uma chamada a **Advise** ter sido bem-sucedida e antes de * * Unadvise * * ter sido chamado, os clientes devem estar preparados para que o objeto de coletor de aviso seja liberado. No entanto, um cliente deve liberar seu objeto **** de coletor de aviso após a revisor, a menos que tenha um uso específico de longo prazo para ele. 
  
Devido ao comportamento assíncrono da notificação, as implementações que alteram as configurações de coluna da tabela podem receber notificações com informações organizadas em uma ordem de coluna anterior. Por exemplo, uma linha de tabela pode ser retornada para uma mensagem que acabou de ser excluída do contêiner. Tal notificação é enviada quando a alteração da configuração da coluna tiver sido feita e informações sobre ela enviadas, mas a exibição da tabela de notificação ainda não tiver sido atualizada com essas informações.
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). Para obter informações específicas sobre a notificação de tabela, consulte [about Table Notifications](about-table-notifications.md). Para obter informações sobre como usar os métodos **IMAPISupport** para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContestTableListCtrl:: notificação  <br/> |MFCMAPI usa o método imApitable **:: Advise** para registrar notificações para permitir que o modo de exibição de tabela permaneça atualizado.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

