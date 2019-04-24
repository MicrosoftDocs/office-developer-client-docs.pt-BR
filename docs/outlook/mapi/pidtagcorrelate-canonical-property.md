---
title: Propriedade canônica PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357915"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propriedade canônica PidTagCorrelate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se o remetente de uma mensagem solicita o recurso de correlação do sistema de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CORRELATE  <br/> |
|Identificador:  <br/> |0x0E0C  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para solicitar a correlação de relatórios de entrada com a mensagem original enviada. Quando um provedor de transporte encontra uma mensagem enviada com o **PR_CORRELATE** definido como true, ele define a propriedade **PR_CORRELATE_MTSID** ([PIDTAGCORRELATEMTSID](pidtagcorrelatemtsid-canonical-property.md)) como o identificador MTS (sistema de transferência de mensagens) para essa mensagem.
  
 **PR_CORRELATE** deve ser usado com sistemas de mensagens que suportam a correlação pelo identificador MTS, como X. 400. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

