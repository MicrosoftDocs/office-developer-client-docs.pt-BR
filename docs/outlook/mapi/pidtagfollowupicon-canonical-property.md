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
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316279"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Propriedade canônica PidTagFollowupIcon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a cor do sinalizador do objeto Message.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificador:  <br/> |0x1095  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |ReNomear pasta de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não deve existir, a menos que o valor da propriedade **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) seja definido como "followupFlagged" ou o objeto Message seja um objeto relacionado à reunião. Esta propriedade não deve existir em um objeto Task. Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos valores a seguir.
  
|**Valor numérico**|**Nome**|**Descrição**|
|:-----|:-----|:-----|
|Não está presente  <br/> |N/D  <br/> |Sem cor  <br/> |
|1  <br/> |followupIcon1  <br/> |Sinalizador roxo  <br/> |
|duas  <br/> |followupIcon2  <br/> |Sinalizador laranja  <br/> |
|3D  <br/> |followupIcon3  <br/> |Sinalizador verde  <br/> |
|quatro  <br/> |followupIcon4  <br/> |Sinalizador amarelo  <br/> |
|0,5  <br/> |followupIcon5  <br/> |Sinalizador azul  <br/> |
|6  <br/> |followupIcon6  <br/> |Sinalizador vermelho  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

