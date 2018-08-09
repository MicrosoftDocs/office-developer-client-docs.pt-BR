---
title: Propriedade canônica PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d91ed369b3a6e8b4f62534d49b202b46c327baa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769046"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propriedade canônica PidTagCommonViewsEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém o identificador de entrada da pasta de exibição comuns predefinidos. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificador:  <br/> |0x35E6  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

A pasta de exibição comuns contém um conjunto predefinido de especificadores de exibição padrão, enquanto a pasta de exibição contém especificadores definidas por um usuário de mensagens. Essas pastas, que não são visíveis na hierarquia de mensagem interpessoais (IPM), podem conter várias especificadores de exibição, cada uma delas armazenada como uma mensagem. Um aplicativo cliente pode optar por mesclar os dois conjuntos de especificadores e disponibilizá-los ambos. 
  
Para obter mais informações sobre modos de exibição, consulte [Exibir pastas](mapi-view-folders.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagDefaultViewEntryId Canonical](pidtagdefaultviewentryid-canonical-property.md)
  
[Propriedade canônica PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

