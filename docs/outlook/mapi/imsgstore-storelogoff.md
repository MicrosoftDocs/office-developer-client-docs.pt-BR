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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424333"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Habilita o logoff ordenar do armazenamento de mensagens.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in, out] Uma máscara de bits de sinalizadores que controla o logoff do armazenamento de mensagens. Na entrada, todos os sinalizadores definidos para esse parâmetro são mutuamente exclusivos; um chamador deve especificar apenas um sinalizador por chamada. Os sinalizadores a seguir são válidos na entrada:
    
LOGOFF_ABORT 
  
> Qualquer atividade do provedor de transporte para este armazenamento de mensagens deve ser interrompida antes de fazer logoff. O controle é retornado ao chamador após a atividade ser interrompida. Se qualquer atividade do provedor de transporte estiver ocorrendo, o logoff não ocorrerá e nenhuma alteração no comportamento do spooler MAPI ou dos provedores de transporte ocorrerá. Se a atividade do provedor de transporte estiver ociosa, o spooler MAPI liberará o armazenamento. 
    
LOGOFF_NO_WAIT 
  
> O armazenamento de mensagens não deve esperar por mensagens de provedores de transporte antes de fechar. As mensagens de saída que estão prontas para serem enviadas são enviadas. Se esse armazenamento contiver a Caixa de Entrada padrão, todas as mensagens em processo serão recebidas e, em seguida, a recepção posterior será desabilitada. Quando todas as atividades são concluídas, o spooler MAPI libera o armazenamento e o controle é retornado imediatamente ao chamador. 
    
LOGOFF_ORDERLY 
  
> O armazenamento de mensagens não deve esperar por informações dos provedores de transporte antes de fechar. As mensagens que estão sendo processadas no momento são concluídas, mas nenhuma mensagem nova é processada. Quando todas as atividades são concluídas, o spooler MAPI libera o armazenamento e o controle é retornado imediatamente ao provedor de armazenamento. 
    
LOGOFF_PURGE 
  
> O logoff deve funcionar da mesma forma como se o sinalizador LOGOFF_NO_WAIT estivesse definido, mas o método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) ou [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) para os provedores de transporte apropriados deve ser chamado. O LOGOFF_PURGE sinalizador retorna o controle ao chamador após a conclusão. 
    
LOGOFF_QUIET 
  
> Se qualquer atividade do provedor de transporte estiver ocorrendo, o logoff não deve ocorrer.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> As mensagens de entrada estão chegando no momento.
    
LOGOFF_OUTBOUND 
  
> As mensagens de saída estão sendo enviadas.
    
LOGOFF_OUTBOUND_QUEUE 
  
> As mensagens de saída estão pendentes (ou seja, estão na Caixa de Saída).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O logoff foi concluído com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::StoreLogoff** exerce controle sobre a interação do repositório de mensagens e dos provedores de transporte durante o processo de logoff. Chamar **StoreLogoff** só é válido para armazenamentos de mensagens que estão sendo usados somente pelo chamador. Por exemplo, quando dois clientes estão usando o mesmo armazenamento de mensagens e um deles chama **StoreLogoff**, o armazenamento de mensagens é liberado imediatamente e o controle é retornado ao cliente de chamada.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Salve os sinalizadores que são passados para **StoreLogoff** e passe-os quando você chamar o método [IMAPISupport::StoreLogoffTransports.](imapisupport-storelogofftransports.md) Não chame **StoreLogoffTransports** até que a contagem de referência do armazenamento de mensagens cai para zero. Várias chamadas para **StoreLogoffTransports** simplesmente sobrescrevem os sinalizadores salvos. 
  
Se nenhuma chamada tiver sido feita para **StoreLogoff** antes que a contagem de referência do armazenamento de mensagens atinja zero, defina o sinalizador LOGOFF_ABORT no  _parâmetro ulFlags_ que você passa para **StoreLogoffTransports**.
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

