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
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418511"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propriedade canônica PidTagStatusCode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de sinalizadores que indicam o status atual de um recurso de sessão. Todos os provedores de serviços configuram códigos de status, assim como o MAPI para relatar o status do subsistema, o spooler MAPI e o livro de endereços integrado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STATUS_CODE  <br/> |
|Identificador:  <br/> |0x3E04  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O código de status deve aparecer no arquivo Mapisvc.inf para todos os provedores. 
  
Os objetos de status são implementados por MAPI e por todos os provedores de serviços. Há dois conjuntos de valores válidos para códigos de status, um conjunto para todos os objetos de status e outro conjunto apenas para provedores de transporte. Todos os objetos de status podem definir essa propriedade com os seguintes valores:
  
STATUS_AVAILABLE 
  
> Indica que o recurso está operacional.
    
STATUS_FAILURE 
  
> Indica que o recurso está enfrentando um problema. Para provedores de serviços, STATUS_FAILURE indica que o provedor poderá ser desligado em breve para encerrar a sessão atual.
    
STATUS_OFFLINE 
  
> Indica que somente os dados ou serviços locais estão disponíveis.
    
Os provedores de transporte também podem definir as propriedades de PR_STATUS_CODE **status** para os seguintes valores: 
  
STATUS_INBOUND_ACTIVE 
  
> Indica que o provedor de transporte está recebendo uma mensagem de entrada. 
    
STATUS_INBOUND_ENABLED 
  
> Indica que o provedor de transporte pode receber mensagens de entrada.
    
STATUS_INBOUND_FLUSH 
  
> Indica que o provedor de transporte está baixando mensagens da fila de entrada.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indica que o provedor de transporte está recebendo uma mensagem de saída. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indica que o provedor de transporte pode lidar com mensagens de saída.
    
STATUS_OUTBOUND_FLUSH 
  
> Indica que o provedor de transporte está carregando mensagens da fila de saída.
    
STATUS_REMOTE_ACCESS 
  
> Indica que o provedor de transporte oferece suporte ao acesso remoto.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

