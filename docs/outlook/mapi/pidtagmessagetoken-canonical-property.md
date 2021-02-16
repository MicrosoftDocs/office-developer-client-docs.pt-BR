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
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408184"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Propriedade canônica PidTagMessageToken

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um token de segurança ASN.1 para uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Identificador:  <br/> |0x0C03  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de Mensagens Seguras  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade transmite informações protegidas relacionadas à segurança de seu originador para seu destinatário. Em conjunto com a **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), ela garante a associação do rótulo com o conteúdo da mensagem. Em conjunto com a **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), verifica se o conteúdo da mensagem não foi alterado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

