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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421379"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita a liberação pedido de um armazenamento de mensagens.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in, out] Uma máscara de bits de sinalizadores que controla como ocorre o logoff do armazenamento de mensagens. Na entrada, todos os sinalizadores para esse parâmetro são mutuamente exclusivos; apenas um dos sinalizadores a seguir pode ser definido por chamada:
    
LOGOFF_ABORT 
  
> Qualquer atividade do provedor de transporte para este armazenamento deve ser interrompida antes de fazer logoff. O controle é retornado ao cliente depois que a atividade é interrompida e o spooler MAPI saiu do armazenamento. Se qualquer atividade de transporte estiver ocorrendo, o logoff não ocorrerá e nenhuma alteração no spooler MAPI ou no comportamento do provedor de transporte ocorrerá. Se não houver nenhuma atividade no momento, o spooler MAPI liberará o armazenamento. 
    
LOGOFF_NO_WAIT 
  
> O spooler MAPI deve liberar o armazenamento e retornar o controle para o cliente imediatamente após o envio de todos os emails de saída que estão prontos para serem enviados. Se o armazenamento de mensagens tiver a Caixa de Entrada padrão, qualquer mensagem no processo será recebida e, em seguida, a recepção posterior será desabilitada. 
    
LOGOFF_ORDERLY 
  
> O spooler MAPI deve liberar o armazenamento e retornar o controle para o cliente imediatamente depois que qualquer mensagem pendente terminar o processamento. Nenhuma mensagem nova deve ser processada. 
    
LOGOFF_PURGE 
  
> Funciona da mesma forma que o LOGOFF_NO_WAIT sinalizador. O LOGOFF_PURGE sinalizador retorna o controle ao chamador após a conclusão. 
    
LOGOFF_QUIET 
  
> O logoff não deve ocorrer se qualquer atividade do provedor de transporte estiver ocorrendo. O tipo de atividade que está ocorrendo é retornado como um sinalizador na saída.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> O logoff pode ser concluído. Todos os recursos associados ao armazenamento foram liberados e o objeto foi invalidado. O spooler MAPI realizou ou executará todas as solicitações. Somente o método **IUnknown::Release** do armazenamento de mensagens deve ser chamado neste ponto. 
    
LOGOFF_INBOUND 
  
> No momento, uma mensagem está chegando à loja de um ou mais provedores de transporte. 
    
LOGOFF_OUTBOUND 
  
> No momento, uma mensagem está sendo enviada da loja por um ou mais provedores de transporte. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Atualmente, há mensagens na fila de saída para o armazenamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O procedimento de logoff foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::StoreLogoffTransports** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens chamam **StoreLogoffTransports** para dar aos aplicativos cliente algum controle sobre como o MAPI lida com a atividade do provedor de transporte à medida que um armazenamento de mensagens está sendo fechado. 
  
Se outro processo faz com que o armazenamento seja desconectado para o mesmo perfil, MAPI ignora uma chamada para **StoreLogoffTransports** e retorna o LOGOFF_COMPLETE sinalizador no parâmetro _lpulFlags._ 
  
O comportamento do provedor de armazenamento após o retorno de **StoreLogoffTransports** deve ser baseado no valor de  _lpulFlags_, que indica o status do sistema e transmite instruções do cliente para o comportamento de logoff. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **StoreLogoffTransports** normalmente é chamado a partir do método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) de um provedor de repositório. No entanto, ele também pode ser chamado a partir do **método IUnknown::Release** do armazenamento de mensagens. Implemente **o método Release** do seu armazenamento de mensagens para que você possa verificar se ocorreu ou não uma chamada para **StoreLogoffTransports.** Se não tiver ocorrido uma chamada, chame **StoreLogoffTransports** com o sinalizador LOGOFF_ABORT definido. 
  
O  _parâmetro lpulFlags_ é definido como um sinalizador que indica como o cliente exige que o armazenamento de mensagens seja desligado. Determine a configuração apropriada para  _ulFlags_ com base na configuração do parâmetro correspondente na chamada para **StoreLogoff**. Ou seja, se um cliente chamado seu método **StoreLogoff** com  _ulFlags_ definido como LOGOFF_ORDERLY, você deve chamar **StoreLogoffTransports** com  _ulFlags_ definido como LOGOFF_ORDERLY. 
  
Para obter mais informações sobre o processo de logoff do armazenamento de mensagens, consulte [Desligar um Provedor de Armazenamento de Mensagens.](shutting-down-a-message-store-provider.md)
  
## <a name="see-also"></a>Confira também



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

