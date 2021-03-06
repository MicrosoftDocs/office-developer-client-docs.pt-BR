---
title: Propriedade canônica PidTagMiniicon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405412"
---
# <a name="pidtagminiicon-canonical-property"></a>Propriedade canônica PidTagMiniicon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um bitmap de um ícone de tamanho médio para um formulário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MINI_ICON  <br/> |
|Identificador:  <br/> |0x0FFC  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém uma imagem de 32 × 32 pixels de um ícone, o mesmo que o conteúdo de um . Arquivo ICO, mas apenas a parte superior esquerda 16 × 16 pixels são consideradas significativas. Essa propriedade normalmente é copiada do . Arquivo ICO especificado na linha SmallIcon da seção [Descrição] apropriada do arquivo de configuração do formulário.
  
 **Observação** Algumas plataformas não suportam ícones de 16 × de 16 pixels. O formato 32 × 32 dessa propriedade pode ser usada nesse caso, mas os aplicativos cliente devem estar cientes das inconsistências de exibição. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagIcon](pidtagicon-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

