---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326492"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita o lançamento ordenada de um repositório de mensagens.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in, out] Uma bitmask de sinalizadores que controlam como o logoff do repositório de mensagens ocorre. Na entrada, todos os sinalizadores desse parâmetro são mutuamente exclusivos; apenas um dos seguintes sinalizadores pode ser definido por chamada:
    
LOGOFF_ABORT 
  
> Qualquer atividade do provedor de transporte para este repositório deve ser interrompida antes do logoff. O controle é retornado ao cliente após a atividade ser interrompida e o spooler MAPI desconectado do repositório. Se alguma atividade de transporte estiver ocorrendo, o logoff não ocorrerá e não ocorrerá nenhuma alteração no comportamento do spooler MAPI ou do provedor de transporte. Se não houver atividade no momento, o spooler MAPI libera o repositório. 
    
LOGOFF_NO_WAIT 
  
> O spooler MAPI deve liberar a loja e retornar o controle para o cliente imediatamente após todos os emails de saída que estão prontos para serem enviados são enviados. Se o repositório de mensagens tiver a caixa de entrada padrão, qualquer mensagem em andamento será recebida e, em seguida, a recepção será desabilitada. 
    
LOGOFF_ORDERLY 
  
> O spooler MAPI deve liberar o armazenamento e retornar o controle para o cliente imediatamente após a conclusão do processamento de qualquer mensagem pendente. Nenhuma mensagem nova deve ser processada. 
    
LOGOFF_PURGE 
  
> Funciona da mesma maneira que o sinalizador LOGOFF_NO_WAIT. O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão. 
    
LOGOFF_QUIET 
  
> O logoff não deve ocorrer se qualquer atividade do provedor de transporte estiver ocorrendo. O tipo de atividade que está sendo realizada é retornado como um sinalizador na saída.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> O logoff pode ser concluído. Todos os recursos associados ao repositório foram liberados e o objeto foi invalidado. O spooler MAPI executou ou executará todas as solicitações. Somente o método **IUnknown:: Release** do repositório de mensagens deve ser chamado neste ponto. 
    
LOGOFF_INBOUND 
  
> No momento, uma mensagem está chegando ao repositório de um ou mais provedores de transporte. 
    
LOGOFF_OUTBOUND 
  
> No momento, uma mensagem está sendo enviada da loja por um ou mais provedores de transporte. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Há mensagens no momento na fila de saída para o repositório.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O procedimento de logoff foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: StoreLogoffTransports** é implementado para objetos de suporte do provedor de repositório de mensagens. Os provedores de repositório de mensagens chamam o **StoreLogoffTransports** para fornecer aos aplicativos cliente controle sobre como o MAPI lida com a atividade do provedor de transporte, pois um repositório de mensagens está fechando. 
  
Se outro processo tiver o repositório a ser conectado aberto para o mesmo perfil, o MAPI ignorará uma chamada para **StoreLogoffTransports** e retornará o sinalizador LOGOFF_COMPLETE no parâmetro _lpulFlags_ . 
  
O comportamento do provedor de repositório após o retorno de **StoreLogoffTransports** deve se basear no valor de _lpulFlags_, que indica o status do sistema e transmite instruções do cliente para o comportamento de logoff. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **StoreLogoffTransports** normalmente é chamado de um método [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) do provedor de repositório. No enTanto, ele também pode ser chamado a partir do método **IUnknown:: Release** do repositório de mensagens. Implemente o método **Release** do seu repositório de mensagens para que você possa verificar se uma chamada para **StoreLogoffTransports** ocorreu ou não. Se uma chamada não tiver ocorrido, chame **StoreLogoffTransports** com o sinalizador LOGOFF_ABORT definido. 
  
O parâmetro _lpulFlags_ é definido como um sinalizador que indica como o cliente exige que o repositório de mensagens seja desligado. Determine a configuração apropriada para o _parâmetroulflags_ com base na configuração do parâmetro correspondente na chamada para **StoreLogoff**. Ou seja, se um cliente chamou o método **StoreLogoff** com _PARÂMETROULFLAGS_ definido como LOGOFF_ORDERLY, você deve chamar **STORELOGOFFTRANSPORTS** com _parâmetroulflags_ definido como LOGOFF_ORDERLY. 
  
Para obter mais informações sobre o processo de logoff do repositório de mensagens, consulte desLigando [um provedor de armazenamento de mensagens](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Confira também



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

