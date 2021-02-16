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
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359490"
---
# <a name="pidtagruleid-canonical-property"></a>Propriedade canônica PidTagRuleId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um identificador exclusivo que o servidor de mensagens gera para cada regra quando a regra é criada pela primeira vez. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULE_ID  <br/> |
|Identificador:  <br/> |0x6674  <br/> |
|Tipo de dados:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Regras do lado do servidor  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente não deve especificar essa propriedade ao criar uma nova regra, mas deve especificá-la ao modificar ou excluir uma regra.
  
Ao excluir uma regra, a única propriedade  que o cliente deve passar é PR_RULE_ID e não deve passar em nenhuma outra propriedade. O servidor deve ignorar propriedades diferentes dessa propriedade. Ao adicionar uma regra, o cliente não deve passar no **PR_RULE_ID**, ele deve passar as propriedades **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) e **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)). Ao modificar uma regra, o  cliente deve passar PR_RULE_ID e deve passar o restante das propriedades que precisam ser modificadas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula mensagens de email de entrada em um servidor.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Propriedade canônica PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Propriedade canônica PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

