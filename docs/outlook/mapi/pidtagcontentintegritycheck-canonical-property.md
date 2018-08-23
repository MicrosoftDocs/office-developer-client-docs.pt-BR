---
title: Propriedade canônica PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 53226daafd1c0a53f96db5af3432d6f34738fd93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585805"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Propriedade canônica PidTagContentIntegrityCheck

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de verificação de integridade do conteúdo de ASN. 1 que permite que um remetente da mensagem proteger o conteúdo da mensagem do divulgação para destinatários não autorizados.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Identificador:  <br/> |0x0C00  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade oferece para não-recusa do conteúdo da mensagem. Em conjunto com **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), ele garante que o conteúdo de uma mensagem chega ao seu destino inalterado.
  
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

