---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348738"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite o logoff ordenada do repositório de mensagens.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in, out] Uma bitmask de sinalizadores que controla o logoff do repositório de mensagens. Na entrada, todos os sinalizadores definidos para esse parâmetro são mutuamente exclusivos; um chamador deve especificar apenas um sinalizador por chamada. Os seguintes sinalizadores são válidos na entrada:
    
LOGOFF_ABORT 
  
> Qualquer atividade do provedor de transporte para esse repositório de mensagens deve ser interrompida antes do logoff. O controle é retornado ao chamador após a interrupção da atividade. Se alguma atividade de provedor de transporte estiver ocorrendo, o logoff não ocorrerá e não ocorrerá alteração no comportamento do spooler MAPI ou provedores de transporte. Se a atividade do provedor de transporte estiver ociosa, o spooler MAPI libera o repositório. 
    
LOGOFF_NO_WAIT 
  
> O repositório de mensagens não deve aguardar mensagens de provedores de transporte antes de fechar. São enviadas mensagens de saída prontas para envio. Se esse repositório contiver a caixa de entrada padrão, qualquer mensagem em andamento será recebida e, em seguida, a recepção estará desabilitada. Quando toda a atividade é concluída, o spooler MAPI libera o repositório e o controle é imediatamente retornado para o chamador. 
    
LOGOFF_ORDERLY 
  
> O repositório de mensagens não deve aguardar informações de provedores de transporte antes de fechar. As mensagens que estão sendo processadas atualmente foram concluídas, mas nenhuma mensagem nova é processada. Quando toda a atividade é concluída, o spooler MAPI libera o repositório e o controle é imediatamente retornado ao provedor de repositório. 
    
LOGOFF_PURGE 
  
> O logoff deve funcionar da mesma forma que se o sinalizador LOGOFF_NO_WAIT estiver definido, mas o método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ou [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) para os provedores de transporte apropriados deverá ser chamado. O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão. 
    
LOGOFF_QUIET 
  
> Se alguma atividade do provedor de transporte estiver ocorrendo, o logoff não deve ocorrer.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> As mensagens de entrada estão chegando no momento.
    
LOGOFF_OUTBOUND 
  
> As mensagens de saída estão no processo de envio.
    
LOGOFF_OUTBOUND_QUEUE 
  
> As mensagens de saída estão pendentes (ou seja, elas estão na mensagem de saída).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O logoff foi concluído com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: StoreLogoff** exerce controle sobre a interação do armazenamento de mensagens e dos provedores de transporte durante o processo de logoff. Chamar **StoreLogoff** é válido somente para repositórios de mensagens que estão sendo usados apenas pelo chamador. Por exemplo, quando dois clientes estão usando o mesmo repositório de mensagens e um deles chama **StoreLogoff**, o repositório de mensagens é lançado imediatamente e o controle é retornado ao cliente de chamada.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Salve os sinalizadores passados para **StoreLogoff** e passe-os quando chamar o método [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) . Não chame **StoreLogoffTransports** até que a contagem de referência do repositório de mensagens descarte para zero. Várias chamadas para **StoreLogoffTransports** simplesmente substituem os sinalizadores salvos. 
  
Se nenhuma chamada tiver sido feita ao **StoreLogoff** antes que a contagem de referência do repositório de mensagens atinja zero, defina o sinalizador LOGOFF_ABORT no parâmetro _parâmetroulflags_ que você passa para **StoreLogoffTransports**.
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

