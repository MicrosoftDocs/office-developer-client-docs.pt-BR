---
title: Propriedade canônica PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421561"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propriedade canônica PidTagStatusString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma mensagem que indica o status atual de um recurso de sessão. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificador:  <br/> |0x3E08  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades oferecem aos provedores de serviços e MAPI a oportunidade de fornecer informações específicas sobre o status de um recurso de sessão, como o catálogo de endereços integrado ou um determinado provedor de serviços. Esta propriedade explica e fornece informações adicionais sobre um código de status ou a propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Enquanto **PR_STATUS_CODE** é necessário para todos os objetos status, **PR_STATUS_STRING** e propriedades associadas são opcionais. Quando o provedor de transporte não fornece um valor, o spooler MAPI fornece um valor padrão. 
  
A cadeia de caracteres é gerada no mesmo lado da chamada de procedimento remoto como o spooler MAPI; Ele passa por memória compartilhada, em vez de ser empacotado em um limite de processo.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

