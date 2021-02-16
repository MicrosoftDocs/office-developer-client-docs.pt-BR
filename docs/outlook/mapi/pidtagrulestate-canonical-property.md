---
title: Propriedade canônica PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338609"
---
# <a name="pidtagrulestate-canonical-property"></a>Propriedade canônica PidTagRuleState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um valor interpretado como uma combinação de bitmask de sinalizadores que especificam o estado da regra.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULE_STATE  <br/> |
|Identificador:  <br/> |0x6677  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Regras do lado do servidor  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir define os valores possíveis dessa propriedade.
  
EN (ST_ENABLED, bitmask 0x00000001)
  
> A regra está habilitada para execução. Se esse sinalizador não estiver definido, o servidor deverá ignorar essa regra ao avaliar as regras.
    
ER (ST_ERROR, máscara de 0x00000002)
  
> O servidor encontrou um erro ao processar a regra.
    
OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)
  
> A regra é executada somente quando o usuário define o estado de Fora do Escritório (OOF) na caixa de correio. Esse sinalizador não deve ser definido em uma regra de pasta pública.
    
HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)
  
> Esse sinalizador não deve ser definido em uma regra de pasta pública.
    
EL (ST_EXIT_LEVEL, bitmask 0x00000010)
  
> A avaliação de regra terminará após a execução dessa regra, exceto para a avaliação das regras de Desem posse.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)
  
> A avaliação dessa regra pode ser ignorada.
    
PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)
  
> O servidor encontrou um erro ao analisar os dados de regra fornecidos pelo cliente.
    
X
  
> Não éusado por este protocolo. Este bit não deve ser modificado pelo cliente.
    
Observação sobre a interação entre ST_ONLY_WHEN_OOF e ST_EXIT_LEVEL sinalizadores: 
  
Quando o estado "Fora do Escritório" é definido na caixa de correio e uma condição de regra é avaliada como VERDADEIRO, 
  
E:
  
- A regra tem o ST_EXIT_LEVEL sinalizador definido e não tem ST_ONLY_WHEN_OOF sinalizador definido. Em seguida, o servidor não deve avaliar as regras subsequentes que não têm um sinalizador ST_ONLY_WHEN_OOF definido e deve avaliar as regras subsequentes que ST_ONLY_WHEN_OOF sinalizador definido.
    
OU:
  
- A regra tem os sinalizadores ST_EXIT_LEVEL e ST_ONLY_WHEN_OOF definidos. Em seguida, o servidor não deve avaliar as regras subsequentes.
    
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



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

