---
title: Propriedade canônica PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316293"
---
# <a name="pidtagflagstatus-canonical-property"></a>Propriedade canônica PidTagFlagStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o estado de sinalizador do objeto Message.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FLAG_STATUS  <br/> |
|Identificador:  <br/> |0x1090  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não deve existir em um objeto relacionado à reunião e não deve existir em um objeto Task. Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos seguintes valores:
  
|**Valor numérico**|**Nome**|**Descrição**|
|:-----|:-----|:-----|
|Não está presente  <br/> |N/D  <br/> |Não sinalizado  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Sinalizador concluído  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Indicado  <br/> |
   
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

