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
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437305"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Propriedade canônica PidTagPstPathHint

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece o nome da tabela de armazenamento pessoal (arquivo. pst), que o usuário pode editar, para a caixa de diálogo de configuração. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Identificador:  <br/> |0x6771  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Tabela de armazenamento pessoal (. pst) interna  <br/> |
   
## <a name="remarks"></a>Comentários

Se a propriedade **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) for usada em vez disso, a caixa de diálogo de configuração será aberta, mas o usuário não poderá editar o caminho e muitas outras propriedades.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]] 
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

