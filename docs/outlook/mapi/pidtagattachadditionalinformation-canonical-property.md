---
title: Propriedade canônica PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339869"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>Propriedade canônica PidTagAttachAdditionalInformation

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações de tipo de arquivo para um anexo não Windows.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Identificador:  <br/> |0x370F  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade fornece metadados sobre um anexo específico com base na codificação do anexo. Por exemplo, quando a propriedade **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contém MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contém uma cadeia de caracteres que representa o criador e o tipo de arquivo do Macintosh, formatado como ": CREA: tipo" para o arquivo de Macintosh codificado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
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

