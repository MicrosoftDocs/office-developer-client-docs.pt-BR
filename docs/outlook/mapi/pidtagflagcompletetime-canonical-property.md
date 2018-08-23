---
title: Propriedade canônica PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6e1c2783abd186146fe738a3396e098711893d3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583978"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>Propriedade canônica PidTagFlagCompleteTime

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a data e hora em tempo Universal Coordenado (UTC) que o objeto de mensagem foi sinalizado como concluída.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|Identificador:  <br/> |0x1091  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é excluída se o objeto de mensagem não foi sinalizado completa. Resolução menor do tempo deve ser minutos (o valor deve ser um múltiplo de 600,000,000). Essa propriedade não deve existir se o objeto é um objeto de reuniões, e ele não deve existir em um objeto task.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
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

