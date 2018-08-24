---
title: Propriedade canônica PidTagMiniIcon
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
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589774"
---
# <a name="pidtagminiicon-canonical-property"></a>Propriedade canônica PidTagMiniIcon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um bitmap de um ícone de meia largura para um formulário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MINI_ICON  <br/> |
|Identificador:  <br/> |0x0FFC  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém uma imagem de 32 × 32 pixels de um ícone, o mesmo que o conteúdo de um. Arquivo ICO, mas apenas os pixels da parte superior esquerda 16 × 16 são considerados significativa. Essa propriedade normalmente é copiada do. Arquivo ICO especificado na linha SmallIcon da seção apropriada [descrição] do arquivo de configuração de formulário.
  
 **Observação** Algumas plataformas fazer não o suporte a 16 × 16 pixels ícones. O formato de 32 × 32 dessa propriedade é utilizável nesse caso, mas os aplicativos cliente devem estar cientes de inconsistências de exibição. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagIcon](pidtagicon-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

