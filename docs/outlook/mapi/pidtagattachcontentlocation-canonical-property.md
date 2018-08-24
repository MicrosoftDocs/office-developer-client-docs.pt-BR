---
title: Propriedade canônica PidTagAttachContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594765"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a>Propriedade canônica PidTagAttachContentLocation

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o cabeçalho de local do conteúdo de anexo de uma mensagem de email extensões MIME (Multipurpose Internet). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W  <br/> |
|Identificador:  <br/> |0x3713  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são usadas para suporte MHTML. Eles representam o cabeçalho de local do conteúdo para a parte apropriada do corpo MIME. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

