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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767507"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Aplica-se a**: Outlook 
  
Habilita o logoff ordenado o armazenamento de mensagens.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpulFlags_
  
> [além, out] Uma bitmask dos sinalizadores que controla o logoff do repositório de mensagem. Na entrada, todos os sinalizadores definido para este parâmetro são mutuamente exclusivos; um chamador deve especificar somente um sinalizador por chamada. Sinalizadores a seguir são válidos na entrada:
    
LOGOFF_ABORT 
  
> Qualquer atividade de provedor de transporte para este armazenamento de mensagens deve ser interrompida antes de fazer logoff. Controle é retornado para o chamador após a atividade foi interrompida. Se qualquer atividade de provedor de transporte está ocorrendo, não ocorrerá o logoff e não ocorrerá nenhuma alteração no comportamento dos provedores de transporte ou spooler de MAPI. Se a atividade de provedor de transporte está ociosa, o MAPI spooler libera o repositório. 
    
LOGOFF_NO_WAIT 
  
> O armazenamento de mensagens não deve aguardar para mensagens de provedores de transporte antes de fechar. Mensagens de saída que estão prontas para serem enviados são enviadas. Se esse repositório contiver a caixa de entrada padrão, todas as mensagens de em processo são recebidas e, em seguida, recepção adicional é desabilitada. Quando todas as atividades estiver concluída, o MAPI spooler libera o repositório e controle imediatamente é retornado ao chamador. 
    
LOGOFF_ORDERLY 
  
> O armazenamento de mensagens não deve aguardar para obter informações de provedores de transporte antes de fechar. Mensagens que estão sendo processadas forem concluídas, mas nenhum novas mensagens forem processadas. Quando todas as atividades estiver concluída, o MAPI spooler libera o repositório e controle imediatamente é retornado para o provedor de armazenamento. 
    
LOGOFF_PURGE 
  
> O logoff deve funcionar o mesmo como se o sinalizador LOGOFF_NO_WAIT estiver definido, mas o [IXPLogon::FlushQueues](ixplogon-flushqueues.md) [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) método ou para os provedores de transporte adequado deve ser chamado. O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão. 
    
LOGOFF_QUIET 
  
> Se qualquer atividade de provedor de transporte está ocorrendo, o logoff não deve ocorrer.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Mensagens de entrada chegam no momento.
    
LOGOFF_OUTBOUND 
  
> Mensagens de saída são no processo que está sendo enviada.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Mensagens de saída estão pendentes (ou seja, eles são na caixa de saída).
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O logoff concluído com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IMsgStore::StoreLogoff** exerce controle sobre a interação da mensagem armazenar e provedores de transporte durante o processo de logoff. Chamar **StoreLogoff** é válida apenas para repositórios de mensagem que estão sendo usados somente pelo chamador. Por exemplo, quando dois clientes estão usando o mesmo armazenamento de mensagens e um deles chama **StoreLogoff**, o armazenamento de mensagens é liberado imediatamente e o controle é retornado para o cliente da chamada.
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Salve os sinalizadores que são passados para **StoreLogoff** e passá-las quando você chama o método [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) . Não chame **StoreLogoffTransports** até que a contagem de referência da loja mensagem cai para zero. Várias chamadas para **StoreLogoffTransports** simplesmente substituem os sinalizadores salvos. 
  
Se nenhuma chamada foi feita para **StoreLogoff** antes da mensagem contagem de referência da loja chega a zero, defina o sinalizador LOGOFF_ABORT no parâmetro _ulFlags_ que você passa para **StoreLogoffTransports**.
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

