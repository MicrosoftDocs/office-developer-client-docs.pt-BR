---
title: Propriedade canônica PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 295b20ebc0c41104a8b1c8e46e2064c3ef32f99e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769732"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Propriedade canônica PidTagPstPathHint

  
  
**Aplica-se a**: Outlook 
  
Fornece o nome de tabela (arquivo. pst) do armazenamento pessoal, que o usuário pode editar, para a caixa de diálogo de configuração. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Identificador:  <br/> |0x6771  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Tabela de armazenamento pessoal (. pst) interna  <br/> |
   
## <a name="remarks"></a>Comentários

Se a propriedade **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) for usada em vez disso, a caixa de diálogo de configuração será aberto, mas o usuário não poderão para editar o caminho e muitas outras propriedades.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

