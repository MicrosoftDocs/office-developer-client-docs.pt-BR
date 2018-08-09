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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767308"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Aplica-se a**: Outlook 
  
Solicita a versão ordenada de um repositório de mensagem.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [além, out] Uma bitmask dos sinalizadores que controla como o logoff do repositório de mensagem ocorre. Na entrada, todos os sinalizadores para este parâmetro são mutuamente exclusivos; somente um dos sinalizadores a seguir pode ser definido por chamada:
    
LOGOFF_ABORT 
  
> Qualquer atividade de provedor de transporte para esse repositório deve ser interrompida antes de fazer logoff. Controle é retornado ao cliente após a atividade foi interrompida e o MAPI spooler tiverem feito logoff o repositório. Se qualquer atividade de transporte estiver ocorrendo, não ocorrerá o logoff e não ocorrerá nenhuma alteração no comportamento de provedor de transporte ou spooler MAPI. Se não há atualmente nenhuma atividade, o MAPI spooler libera o repositório. 
    
LOGOFF_NO_WAIT 
  
> O MAPI spooler deve liberar o repositório e retornar o controle para o cliente imediatamente saída depois que todos os emails que está pronta para ser enviada é enviada. Se o armazenamento de mensagens tiver a caixa de entrada padrão, qualquer mensagem em processo é recebida e, em seguida, recepção adicional é desabilitada. 
    
LOGOFF_ORDERLY 
  
> O MAPI spooler deve liberar o repositório e retornar o controle para o cliente imediatamente após pendentes mensagens estiverem terminadas processamento. Não há novas mensagens devem ser processadas. 
    
LOGOFF_PURGE 
  
> Funciona da mesma maneira como o sinalizador LOGOFF_NO_WAIT. O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão. 
    
LOGOFF_QUIET 
  
> O logoff não deve ocorrer se qualquer atividade de provedor de transporte estiver ocorrendo. O tipo de atividade ocorrendo é retornado como um sinalizador na saída.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> O logoff pode concluir. Todos os recursos associados ao repositório foram liberados e o objeto foi invalidado. O MAPI spooler realizou ou irá realizar todas as solicitações. Apenas o método de **IUnknown:: Release** da loja mensagem deve ser chamado neste momento. 
    
LOGOFF_INBOUND 
  
> Uma mensagem atualmente vem para o repositório de um ou mais provedores de transporte. 
    
LOGOFF_OUTBOUND 
  
> Uma mensagem atualmente está sendo enviada do repositório por um ou mais provedores de transporte. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Atualmente existem mensagens na fila de saída para o repositório.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O procedimento de logoff foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::StoreLogoffTransports** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagem chamarem **StoreLogoffTransports** para fornecer aplicativos cliente algum controle sobre como a atividade de provedor de transporte MAPI alças como um armazenamento de mensagens está sendo fechado. 
  
Se outro processo tiver o repositório a ser desconectado de abrir para o mesmo perfil, MAPI ignora uma chamada para **StoreLogoffTransports** e retorna o sinalizador LOGOFF_COMPLETE no parâmetro _lpulFlags_ . 
  
O comportamento do provedor de repositório seguindo o retorno do **StoreLogoffTransports** deve ter como base o valor da _lpulFlags_, que indica o status do sistema e transmite instruções de cliente para o comportamento de logoff. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **StoreLogoffTransports** geralmente é chamado pelo método de [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) um repositório do provedor. No entanto, ele também pode ser chamado pelo método **IUnknown:: Release** o armazenamento de mensagens. Implementar o método de **lançamento** do seu armazenamento de mensagens de modo que você possa verificar se ou não uma chamada para **StoreLogoffTransports** ocorreu. Se uma chamada não tiver ocorrido, chame **StoreLogoffTransports** com o sinalizador LOGOFF_ABORT definido. 
  
O parâmetro _lpulFlags_ é definido como um sinalizador que indica como o cliente requer o armazenamento de mensagens seja encerrado. Determine a configuração apropriada para _ulFlags_ com base na configuração do parâmetro correspondente na chamada a **StoreLogoff**. Ou seja, se um cliente chamado o método **StoreLogoff** com _ulFlags_ definido como LOGOFF_ORDERLY, você deve chamar **StoreLogoffTransports** com _ulFlags_ definido como LOGOFF_ORDERLY. 
  
Para obter mais informações sobre o processo de logoff do repositório de mensagem, consulte [Sendo para baixo uma mensagem Store Provider](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Confira também



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

