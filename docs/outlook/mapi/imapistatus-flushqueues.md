---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592196"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Força todas as mensagens aguardando para ser enviado ou recebido para ser carregadas ou baixadas imediatamente. Os objetos de status que implementam provedores de transporte e o objeto de status do MAPI spooler suportam este método.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.
    
 _cbTargetTransport_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpTargetTransport_ . O parâmetro _cbTargetTransport_ é definido somente em chamadas para objeto de status do MAPI spooler. Para chamadas a um provedor de transporte, o parâmetro _cbTargetTransport_ é definido como 0. 
    
 _lpTargetTransport_
  
> [in] Um ponteiro para o identificador de entrada do provedor de transporte que seja a liberar seus filas de mensagens. O parâmetro _lpTargetTransport_ é definido somente em chamadas para objeto de status do MAPI spooler. Para chamadas a um provedor de transporte, o parâmetro _lpTargetTransport_ é definido como NULL. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a operação de liberação. Sinalizadores a seguir podem ser definidos:
    
FLUSH_ASYNC_OK 
  
> A operação de liberação pode ocorrer assincronamente. Esse sinalizador se aplica somente ao objeto de status do spooler MAPI. 
    
FLUSH_DOWNLOAD 
  
> As filas de mensagens de entrada devem ser liberadas.
    
FLUSH_FORCE 
  
> A operação de liberação deve ocorrer independentemente, apesar da possibilidade de que uma diminuição no desempenho. Esse sinalizador deve ser definida quando um provedor de transporte assíncrono está programado.
    
FLUSH_NO_UI 
  
> O objeto status não deverá exibir um indicador de progresso.
    
FLUSH_UPLOAD 
  
> As filas de mensagens de saída devem ser liberadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de liberação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento. ele deve ter permissão para concluir ou ele deve ser interrompido, antes que esta operação pode ser iniciada.
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não suporta essa operação, conforme indicado pela ausência do sinalizador STATUS_FLUSH_QUEUES na propriedade de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.
    
## <a name="remarks"></a>Comentários

O método **IMAPIStatus::FlushQueues** solicita que o spooler MAPI ou um provedor de transporte imediatamente enviar todas as mensagens na fila de saída ou recebe todas as mensagens da fila de entrada. **FlushQueues** é implementado apenas pelo objeto de status de spooler MAPI e por objetos de status que suprimentos de provedores de transporte. 
  
MAPI_E_BUSY devem ser retornadas para solicitações assíncronas, para que os clientes possam continuar o trabalho. 
  
Por padrão, **FlushQueues** é uma operação síncrona; controle não retorna ao chamador até que a liberação foi concluída. Somente a liberação operação executada pelo spooler MAPI pode ser assíncrona; os clientes solicitam esse comportamento, definindo o sinalizador FLUSH_ASYNC_OK. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Implementação do provedor de um transporte remoto **FlushQueues** define bits na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) na linha de status do objeto logon para controlar como as filas são liberadas. Se um visualizador remoto passa na sinalizar FLUSH_UPLOAD, o método **FlushQueues** deve definir os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE. Se um visualizador remoto passa na sinalizar FLUSH_DOWNLOAD, o método **FlushQueues** deve definir os bits STATUS_OUTBOUND_ENABLED e STATUS_OUTBOUND_ACTIVE. **FlushQueues** , em seguida, deve retornar S_OK. O MAPI spooler então iniciarão as ações apropriadas para carregar e baixar mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Uma chamada para o objeto de status do MAPI spooler é uma diretiva para transferir todas as mensagens de ou o provedor de transporte adequado. Quando você chama o objeto de status de um provedor transporte individual, somente as mensagens desse provedor serão afetadas.
  
## <a name="see-also"></a>Confira também



[Propriedade canônico de PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propriedade canônico de PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

