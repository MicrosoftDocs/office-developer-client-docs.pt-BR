---
title: Propriedade canônica PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2831e31e8139dd2348c2deffa6da41793d0a3f4b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576243"
---
# <a name="pidtagruleid-canonical-property"></a>Propriedade canônica PidTagRuleId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um identificador exclusivo que do servidor de mensagens gera para cada regra quando a regra é criada pela primeira vez. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULE_ID  <br/> |
|Identificador:  <br/> |0x6674  <br/> |
|Tipo de dados:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Regras do lado servidor  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente não deve especificar essa propriedade ao criar uma nova regra, mas deve especificá-lo quando modificar ou excluir uma regra.
  
Ao excluir uma regra, a única propriedade que o cliente deve passar é **PR_RULE_ID** e não deve passar em qualquer outra propriedade. O servidor deve ignorar propriedades que não seja essa propriedade. Ao adicionar uma regra, o cliente não deve passar em **PR_RULE_ID**, ele deve passar na **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) e **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) propriedades. Ao modificar uma regra, o cliente deve passar no **PR_RULE_ID** e deve passar o restante das propriedades que precisam ser modificados. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula mensagens de email de entrada em um servidor.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Propriedade canônica PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Propriedade canônica PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

