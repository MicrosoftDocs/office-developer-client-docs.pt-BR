---
title: Propriedade canônica PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769653"
---
# <a name="pidtagparentdisplay-canonical-property"></a>Propriedade canônica PidTagParentDisplay

  
  
**Aplica-se a**: Outlook 
  
Contém o nome de exibição da pasta onde uma mensagem foi encontrada durante uma pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W  <br/> |
|Identificador:  <br/> |0x0E05  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades não está em qualquer objeto. Eles só podem aparecer na tabela de conteúdo de uma pasta de resultados de pesquisa.
  
Essas propriedades e **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) não estão relacionados entre si. Eles pertencem ao contextos completamente diferentes.
  
## <a name="related-resources"></a>Recursos relacionados

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

