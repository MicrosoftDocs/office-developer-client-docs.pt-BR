---
title: Propriedade canônica PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8fa96736b5404d84c6ab48851b916c5ab987ae2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593918"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Propriedade canônica PidTagFollowupIcon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a cor de sinalizador do objeto de mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificador:  <br/> |0x1095  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Renomear pasta de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não deve existir, a menos que o valor da propriedade **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) é definido como "followupFlagged" ou a mensagem for um objeto de reuniões. Essa propriedade não deve existir em um objeto task. Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos valores a seguir.
  
|**Valor numérico**|**Nome**|**Descrição**|
|:-----|:-----|:-----|
|Não estiver presente  <br/> |N/A  <br/> |Sem cor  <br/> |
|1  <br/> |followupIcon1  <br/> |Sinalizador roxo  <br/> |
|2  <br/> |followupIcon2  <br/> |Sinalizador Laranja  <br/> |
|3  <br/> |followupIcon3  <br/> |Sinalizador verde  <br/> |
|4  <br/> |followupIcon4  <br/> |Sinalizador amarelo  <br/> |
|5  <br/> |followupIcon5  <br/> |Sinalizador azul  <br/> |
|6  <br/> |followupIcon6  <br/> |Sinalizador vermelho  <br/> |
   
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

