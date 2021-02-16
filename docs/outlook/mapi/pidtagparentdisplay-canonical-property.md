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
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429499"
---
# <a name="pidtagparentdisplay-canonical-property"></a>Propriedade canônica PidTagParentDisplay

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de exibição da pasta onde uma mensagem foi encontrada durante uma pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W  <br/> |
|Identificador:  <br/> |0x0E05  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MAPI não transmitível  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades não estão em nenhum objeto. Eles só podem aparecer no índice de uma pasta de resultados de pesquisa.
  
Essas propriedades e **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) não estão relacionadas entre si. Eles pertencem a contextos totalmente diferentes.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

