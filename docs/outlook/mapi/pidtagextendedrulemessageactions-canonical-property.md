---
title: Propriedade canônica PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5425496a5b7845daabf736978e6ed24518451fe0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769247"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>Propriedade canônica PidTagExtendedRuleMessageActions

  
  
**Aplica-se a**: Outlook 
  
Contém informações adicionais sobre as propriedades nomeadas usado em uma mensagem de informações de associado de pasta (FAI).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Identificador:  <br/> |0x0E99  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade deve ser definida em uma mensagem FAI. Esta propriedade tem a mesma finalidade como **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), mas contém informações adicionais sobre a versão das propriedades nomeadas armazenadas na ação da regra e a regra, bem como informações sobre as ações a serem executados por essa regra. Todos os valores de cadeia de caracteres contidos em qualquer parte do buffer de ação usado para conter as ações devem estar no formato Unicode.
  
Para obter informações sobre o formato dessa propriedade binários, consulte [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo do Exchange Server relacionadas..
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula mensagens de email de entrada em um servidor.
    
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

