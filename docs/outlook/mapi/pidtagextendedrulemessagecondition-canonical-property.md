---
title: Propriedade canônica PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316328"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>Propriedade canônica PidTagExtendedRuleMessageCondition

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre as propriedades nomeadas que estão contidas dentro de condições estendidas da regra.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|Identificador:  <br/> |0x0E9A  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Regras  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida em uma mensagem FAI. Ele tem a mesma finalidade que **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), mas contém informações adicionais sobre as propriedades nomeadas usadas. Todos os valores de cadeia de caracteres contidos em qualquer parte deste valor da Propriedade Condition devem estar no formato Unicode.
  
Para obter informações sobre o formato dessa propriedade binária, consulte [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula mensagens de email de entrada em um servidor.
    
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

