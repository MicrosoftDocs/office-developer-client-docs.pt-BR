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
ms.openlocfilehash: fe722e8723fdc3868cbbc3188f03e13ef3f466f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575333"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de fila saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do armazenamento de mensagens. Este método é chamado somente pelo spooler MAPI.
  
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
  
> A tabela de fila de saída foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::GetOutgoingQueue** fornece o MAPI spooler com acesso à tabela que mostra a fila do armazenamento de mensagens de mensagens de saída. Normalmente, as mensagens são colocadas na tabela de fila de saída depois seu método [IMessage::SubmitMessage](imessage-submitmessage.md) é chamado. No entanto, como a ordem de envio afeta a ordem de pré-processamento e o envio para o provedor de transporte, algumas mensagens que foram marcadas para enviar talvez não apareçam na tabela de fila de saída imediatamente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Para obter uma lista das propriedades que devem ser incluídos como colunas em sua tabela de fila de saída, consulte as [Tabelas de fila de saída](outgoing-queue-tables.md). 
  
Como o spooler MAPI foi projetado para aceitar mensagens de um armazenamento de mensagens em ordem crescente de hora de envio, permitir que o spooler MAPI classificar a tabela de fila de saída para que corresponda nesta ordem ou estabelecê-la como a ordem de classificação padrão.
  
Você deve suportar as notificações para a saída tabela de fila de mensagens, garantindo que o MAPI spooler é notificado quando o conteúdo da fila for alterado. 
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

