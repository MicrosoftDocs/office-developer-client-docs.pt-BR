---
title: Propriedade canônica PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427308"
---
# <a name="pidtagviewsentryid-canonical-property"></a>Propriedade canônica PidTagViewsEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada da pasta Views definida pelo usuário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Identificador:  <br/> |0x35E5  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A pasta de exibição comum contém um conjunto predefinido de especificadores de exibição padrão, enquanto a pasta de exibição contém especificadores definidos por um usuário de mensagens. Essas pastas, que não são visíveis na hierarquia de mensagens interpersonales (IPM), podem conter muitos especificadores de exibição, cada um armazenado como uma mensagem. O aplicativo cliente pode optar por mesclar os dois conjuntos de especificadores e torná-los disponíveis.
  
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

