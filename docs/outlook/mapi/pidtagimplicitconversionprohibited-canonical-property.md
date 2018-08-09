---
title: Propriedade canônica PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769347"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Propriedade canônica PidTagImplicitConversionProhibited

  
  
**Aplica-se a**: Outlook 
  
Conterá TRUE se um agente de transferência de mensagem (MTA) é proibido de fazer a mensagem implícita conversões de texto.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Identificador:  <br/> |0x0016  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for TRUE, o sistema de mensagens deve não execute nenhuma conversão de conteúdo na mensagem, a menos que seja solicitado explicitamente em uma base por destinatário com a propriedade **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

