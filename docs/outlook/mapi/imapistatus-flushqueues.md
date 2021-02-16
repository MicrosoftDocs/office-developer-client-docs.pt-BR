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
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432601"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Força que todas as mensagens que aguardam para serem enviadas ou recebidas sejam carregadas ou baixadas imediatamente. O objeto de status do spooler MAPI e os objetos de status que os provedores de transporte implementam suportam esse método.
  
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
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _cbTargetTransport_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpTargetTransport._ O  _parâmetro cbTargetTransport_ é definido somente em chamadas para o objeto de status do spooler MAPI. Para chamadas para um provedor de transporte, o  _parâmetro cbTargetTransport_ é definido como 0. 
    
 _lpTargetTransport_
  
> [in] Um ponteiro para o identificador de entrada do provedor de transporte que deve liberar suas filas de mensagens. O  _parâmetro lpTargetTransport_ é definido somente em chamadas para o objeto de status do spooler MAPI. Para chamadas para um provedor de transporte, o  _parâmetro lpTargetTransport_ é definido como NULL. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a operação de liberação. Os sinalizadores a seguir podem ser definidos:
    
FLUSH_ASYNC_OK 
  
> A operação de liberação pode ocorrer de forma assíncrona. Esse sinalizador se aplica somente ao objeto de status do spooler MAPI. 
    
FLUSH_DOWNLOAD 
  
> As filas de mensagens de entrada devem ser liberados.
    
FLUSH_FORCE 
  
> A operação de liberação deve ocorrer independentemente da probabilidade de uma diminuição no desempenho. Esse sinalizador deve ser definido quando um provedor de transporte assíncrono é direcionado.
    
FLUSH_NO_UI 
  
> O objeto de status não deve exibir um indicador de progresso.
    
FLUSH_UPLOAD 
  
> As filas de mensagens de saída devem ser liberados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de liberação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento; ela deve ter permissão para ser concluída ou deve ser interrompida antes que essa operação possa ser iniciada.
    
MAPI_E_NO_SUPPORT 
  
> O objeto de status não dá suporte a essa operação, conforme indicado pela ausência do sinalizador STATUS_FLUSH_QUEUES na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto de status.
    
## <a name="remarks"></a>Comentários

O **método IMAPIStatus::FlushQueues** solicita que o spooler MAPI ou um provedor de transporte envie imediatamente todas as mensagens na fila de saída ou receba todas as mensagens da fila de entrada. **FlushQueues é** implementado apenas pelo objeto de status do spooler MAPI e pelos objetos de status que os provedores de transporte fornecem. 
  
MAPI_E_BUSY deve ser retornado para solicitações assíncronas para que os clientes possam continuar trabalhando. 
  
Por padrão, **FlushQueues** é uma operação síncrona; não retorna ao chamador até que a liberação seja concluída. Somente a operação de liberação executada pelo spooler MAPI pode ser assíncrona; os clientes solicitam esse comportamento definindo o FLUSH_ASYNC_OK padrão. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação de **FlushQueues** de um provedor de transporte remoto define bits na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) na linha de status do objeto de logon para controlar como as filas são liberados. Se um visualizador remoto passar no sinalizador FLUSH_UPLOAD, o método **FlushQueues** deverá definir os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE bits. Se um visualizador remoto passar no sinalizador FLUSH_DOWNLOAD, o método **FlushQueues** deverá definir os bits STATUS_OUTBOUND_ENABLED e STATUS_OUTBOUND_ACTIVE bits. **FlushQueues** deve retornar S_OK. O spooler MAPI iniciará as ações apropriadas para carregar e baixar mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Uma chamada para o objeto de status do spooler MAPI é uma diretiva para transferir todas as mensagens de ou para o provedor de transporte apropriado. Quando você chama um objeto de status de um provedor de transporte individual, somente as mensagens desse provedor são afetadas.
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propriedade canônica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

