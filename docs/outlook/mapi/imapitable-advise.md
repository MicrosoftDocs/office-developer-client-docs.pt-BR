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
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594240"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um objeto de coletor de eventos advise para receber notificações de eventos especificados que afetam a tabela.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulEventMask_
  
> [in] Valor que indica o tipo de evento que irá gerar a notificação. O seguinte valor só é válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes. Este objeto de coletor de eventos advise deve foram já alocado.
    
 _lpulConnection_
  
> [out] Ponteiro para um valor diferente de zero que representa o registro de notificação bem-sucedida.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro de notificação concluído com êxito.
    
MAPI_E_NO_SUPPORT 
  
> A implementação de tabela não oferece suporte a alterações em suas linhas e colunas ou não oferece suporte a notificação.
    
## <a name="remarks"></a>Comentários

Use o método **IMAPITable::Advise** para registrar um objeto table implementado no provedor para retornos de chamada de notificação. Sempre que ocorre uma alteração ao objeto table, o provedor verifica quais bits de máscara de evento foi definida no parâmetro _ulEventMask_ e, portanto, o tipo de alteração que ocorreu. Se um pouco for definido, o provedor chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto coletor de eventos de advise indicado pelo parâmetro _lpAdviseSink_ para relatar o evento. Dados passados na estrutura de notificação para a rotina de **OnNotify** descrevem o evento. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou a qualquer momento a seguir. Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer segmento. Para ativar uma chamada para **OnNotify** que pode acontecer um inoportunos momento em que é mais seguro lidar com uma maneira, um provedor deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para fornecer notificações, o provedor implementing **Advise** precisa manter uma cópia do ponteiro para o _lpAdviseSink_ avise o objeto coletor de eventos; Para fazer isso, ele chama o método **AddRef** para o coletor de eventos advise manter seu indicador de objeto até que o registro de notificação será cancelado com uma chamada ao método [IMAPITable::Unadvise](imapitable-unadvise.md) . A implementação de **Advise** deve atribuir um número de conexão para o registro de notificação e chamar **AddRef** este número de conexão antes de retorná-lo no parâmetro _lpulConnection_ . Provedores de serviços podem liberar o objeto coletor de eventos advise antes que o registro será cancelado, mas eles não devem liberar o número de conexão até * * Unadvise * * foi chamado. 
  
Depois que uma chamada para **Advise** teve sucesso e antes * * Unadvise * * tenha sido chamado, os clientes devem ser preparados para o objeto coletor de eventos de advise ser liberada. Um cliente, portanto, deve liberar seu objeto de coletor advise depois **Advise** retorna a menos que ele tenha um uso específico de longo prazo para ele. 
  
Devido ao comportamento assíncrono da notificação, implementações que alterar as configurações de coluna de tabela podem receber notificações com informações organizadas em uma ordem de coluna anterior. Por exemplo, uma linha da tabela pode ser retornada por uma mensagem que foi excluída do contêiner. Tal uma notificação é enviada quando foi feita a alteração de configuração de coluna e informações sobre ele enviadas, mas o modo de exibição de tabela de notificação não foi atualizado com essas informações ainda.
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter informações específicas sobre a notificação de tabela, consulte [Sobre notificações de tabela](about-table-notifications.md). Para obter informações sobre como usar os métodos **IMAPISupport** para suportar a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI usa o método **IMAPITable::Advise** para registrar para notificações permitir que o modo de exibição de tabela permaneçam atual.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

