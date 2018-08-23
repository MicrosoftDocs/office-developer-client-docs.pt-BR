---
title: Propriedade canônica PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a60bc55686e883cabd144af3a9badfb55f835472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593120"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propriedade canônica PidTagStatusCode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask dos sinalizadores que indicam o status atual de um recurso de sessão. Todos os provedores de serviço definir códigos de status como MAPI a ser relatado no status do catálogo de endereços integrada, o MAPI spooler e o subsistema de faz.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STATUS_CODE  <br/> |
|Identificador:  <br/> |0x3E04  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O código de status deve aparecer no arquivo Mapisvc para todos os provedores. 
  
Objetos de status são implementados por MAPI e por todos os provedores de serviço. Há dois conjuntos de valores válidos para códigos de status, um conjunto de todos os objetos de status e outro conjunto para apenas os provedores de transporte. Todos os objetos de status podem definir essa propriedade para os seguintes valores:
  
STATUS_AVAILABLE 
  
> Indica se o recurso está em operação.
    
STATUS_FAILURE 
  
> Indica que o recurso está com problemas. Para provedores de serviço, STATUS_FAILURE indica que o provedor talvez breve sejam desligado para terminar a sessão atual.
    
STATUS_OFFLINE 
  
> Indica que os dados apenas locais ou serviços estão disponíveis.
    
Provedores de transporte também podem definir seu status **PR_STATUS_CODE** propriedades dos objetos para os seguintes valores: 
  
STATUS_INBOUND_ACTIVE 
  
> Indica que o provedor de transporte está recebendo uma mensagem de entrada. 
    
STATUS_INBOUND_ENABLED 
  
> Indica que o provedor de transporte pode receber mensagens de entrada.
    
STATUS_INBOUND_FLUSH 
  
> Indica que o provedor de transporte é baixando mensagens da fila de entrada.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indica que o provedor de transporte está recebendo uma mensagem de saída. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indica que o provedor de transporte pode manipular mensagens de saída.
    
STATUS_OUTBOUND_FLUSH 
  
> Indica que o provedor de transporte está carregando mensagens de sua fila de saída.
    
STATUS_REMOTE_ACCESS 
  
> Indica que o provedor de transporte suporta acesso remoto.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

