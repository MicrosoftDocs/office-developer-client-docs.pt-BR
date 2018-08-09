---
title: Propriedade canônica PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769469"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Propriedade canônica PidTagMemberEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém o identificador de entrada de objeto de diretório de um membro de tabela do sistema acesso controle SACL (lista).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Regras do lado servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar exclusivamente uma pessoa ou função aos quais se aplica a SACL. Depois que o membro é criado na tabela a SACL, **ENTRYID** não pode ser alterado. Para alterá-lo, você deve excluir o membro de tabela e recriá-la com um diferentes **ENTRYID**.
  
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

