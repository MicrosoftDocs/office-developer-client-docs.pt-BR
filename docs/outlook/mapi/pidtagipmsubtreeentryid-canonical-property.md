---
title: Propriedade canônica PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769389"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>Propriedade canônica PidTagIpmSubtreeEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém o identificador de entrada da raiz da subárvore pasta interpessoais mensagens (IPM) na árvore de pastas do armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|Identificador:  <br/> |0x35E0  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade representa a raiz da hierarquia IPM. Clientes IPM não deverá exibir quaisquer pastas que não são subpastas da pasta representada por esta propriedade.
  
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

