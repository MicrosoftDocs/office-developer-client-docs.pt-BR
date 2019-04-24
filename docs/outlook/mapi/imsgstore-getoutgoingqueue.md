---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317329"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de fila de saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do repositório de mensagens. Este método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de fila de saída.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de fila de saída foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: GetOutgoingQueue** fornece ao spooler MAPI o acesso à tabela que mostra a fila de mensagens de saída do repositório de mensagens. Normalmente, as mensagens são colocadas na tabela de fila de saída depois que o método [IMessage:: SubmitMessage](imessage-submitmessage.md) é chamado. No enTanto, como a ordem de envio afeta a ordem de pré-processamento e envio para o provedor de transporte, algumas mensagens marcadas para envio podem não aparecer na tabela de fila de saída imediatamente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Para obter uma lista das propriedades que devem ser incluídas como colunas na tabela de fila de saída, confira [tabelas de fila de saída](outgoing-queue-tables.md). 
  
Como o spooler MAPI foi projetado para aceitar mensagens de um repositório de mensagens em ordem crescente de tempo de envio, permita que o spooler MAPI Classifique a tabela de fila de saída para corresponder a essa ordem ou a estabeleça como a ordem de classificação padrão.
  
Você deve dar suporte a notificações para a tabela de fila de mensagens de saída, garantindo que o spooler MAPI seja notificado quando o conteúdo da fila for alterado. 
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

