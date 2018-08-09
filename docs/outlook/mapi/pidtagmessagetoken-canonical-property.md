---
title: Propriedade canônica PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769492"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Propriedade canônica PidTagMessageToken

  
  
**Aplica-se a**: Outlook 
  
Contém um token de segurança de uma mensagem ASN. 1.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Identificador:  <br/> |0x0C03  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de mensagens de seguro  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade transmite protegidas informações relacionadas à segurança do originador ao destinatário. Em conjunto com a propriedade **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), garante a associação do rótulo com o conteúdo da mensagem. Em conjunto com a propriedade **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), ele verifica se o conteúdo da mensagem está inalterado.
  
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

