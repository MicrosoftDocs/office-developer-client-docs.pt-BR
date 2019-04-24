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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328191"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Força todas as mensagens aguardando para serem enviadas ou recebidas para serem carregadas ou baixadas imediatamente. O objeto de status do spooler MAPI e os objetos de status que os provedores de transporte implementam dão suporte a esse método.
  
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
  
> no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _cbTargetTransport_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpTargetTransport_ . O parâmetro _cbTargetTransport_ é definido somente em chamadas para o objeto status do spooler MAPI. Para chamadas para um provedor de transporte, o parâmetro _cbTargetTransport_ é definido como 0. 
    
 _lpTargetTransport_
  
> no Um ponteiro para o identificador de entrada do provedor de transporte que deve liberar suas filas de mensagens. O parâmetro _lpTargetTransport_ é definido somente em chamadas para o objeto status do spooler MAPI. Para chamadas para um provedor de transporte, o parâmetro _lpTargetTransport_ é definido como nulo. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a operação de liberação. Os seguintes sinalizadores podem ser definidos:
    
FLUSH_ASYNC_OK 
  
> A operação de liberação pode ocorrer de forma assíncrona. Este sinalizador se aplica somente ao objeto status do spooler MAPI. 
    
FLUSH_DOWNLOAD 
  
> As filas de mensagens de entrada devem ser liberadas.
    
FLUSH_FORCE 
  
> A operação de liberação deve ocorrer independentemente da chance de uma redução no desempenho. Esse sinalizador deve ser definido quando um provedor de transporte assíncrono é direcionado.
    
FLUSH_NO_UI 
  
> O objeto status não deve exibir um indicador de progresso.
    
FLUSH_UPLOAD 
  
> As filas de mensagens de saída devem ser liberadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de liberação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento; Ele deve ter permissão para ser concluído ou deve ser interrompido antes que essa operação possa ser iniciada.
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não oferece suporte a essa operação, conforme indicado pela ausência do sinalizador STATUS_FLUSH_QUEUES na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.
    
## <a name="remarks"></a>Comentários

O método **IMAPIStatus:: FlushQueues** solicita que o spooler MAPI ou um provedor de transporte envie imediatamente todas as mensagens na fila de saída ou receba todas as mensagens da fila de entrada. **FlushQueues** é implementada apenas pelo objeto de status do spooler MAPI e por objetos de status que os provedores de transporte fornecem. 
  
MAPI_E_BUSY deve ser retornado para solicitações assíncronas para que os clientes possam continuar a trabalhar. 
  
Por padrão, **FlushQueues** é uma operação síncrona; o controle não retorna ao chamador até que a liberação tenha sido concluída. Somente a operação de liberação executada pelo spooler MAPI pode ser assíncrona; Os clientes solicitam esse comportamento definindo o sinalizador FLUSH_ASYNC_OK. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação de um provedor de transporte remoto do **FlushQueues** define bits na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) na linha de status do objeto de logon para controlar como as filas são liberadas. Se um visualizador remoto passar no sinalizador FLUSH_UPLOAD, o método **FlushQueues** deverá definir os bits do STATUS_INBOUND_ENABLED e do STATUS_INBOUND_ACTIVE. Se um visualizador remoto passar no sinalizador FLUSH_DOWNLOAD, o método **FlushQueues** deverá definir os bits do STATUS_OUTBOUND_ENABLED e do STATUS_OUTBOUND_ACTIVE. **FlushQueues** deve retornar S_OK. O spooler MAPI iniciará as ações apropriadas para carregar e baixar mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Uma chamada para o objeto de status MAPI spooler é uma diretiva para transferir todas as mensagens de ou para o provedor de transporte apropriado. Quando você chama o objeto status de um provedor de transporte individual, somente as mensagens desse provedor são afetadas.
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propriedade canônica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

