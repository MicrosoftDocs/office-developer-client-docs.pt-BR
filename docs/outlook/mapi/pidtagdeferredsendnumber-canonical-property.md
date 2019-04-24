---
title: Propriedade canônica PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357733"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>Propriedade canônica PidTagDeferredSendNumber

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um número que pode ser usado para calcular o diferimento do envio de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Identificador:  <br/> |0x3FEB  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para calcular a propriedade **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) quando não estiver presente. Quando o envio de uma mensagem é adiado, a propriedade **PR_DEFERRED_SEND_NUMBER** deve ser definida juntamente com a propriedade **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), se a propriedade **PR_DEFERRED_SEND_TIME** estiver ausente. 
  
O valor **PR_DEFERRED_SEND_NUMBER** deve ser definido entre 0 e 999. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

