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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434148"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de filas de saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do armazenamento de mensagens. Esse método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de fila de saída.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de filas de saída foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::GetOutgoingQueue** fornece ao spooler MAPI acesso à tabela que mostra a fila de mensagens de saída do repositório de mensagens. Normalmente, as mensagens são colocadas na tabela de filas de saída após o método [IMessage::SubmitMessage](imessage-submitmessage.md) ser chamado. No entanto, como a ordem de envio afeta a ordem de pré-processamento e envio ao provedor de transporte, algumas mensagens marcadas para envio podem não aparecer imediatamente na tabela de filas de saída. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Para uma lista das propriedades que devem ser incluídas como colunas em sua tabela de fila de saída, consulte Tabelas de Fila de [Saída.](outgoing-queue-tables.md) 
  
Como o spooler MAPI foi projetado para aceitar mensagens de um armazenamento de mensagens em ordem crescente de tempo de envio, permita que o spooler MAPI classificar a tabela de fila de saída para corresponder a essa ordem ou estabeleça-a como a ordem de classificação padrão.
  
Você deve dar suporte a notificações para a tabela de fila de mensagens de saída, garantindo que o spooler MAPI seja notificado quando o conteúdo da fila mudar. 
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

