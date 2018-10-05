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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395424"
---
# <a name="pidtagrulestate-canonical-property"></a>Propriedade canônica PidTagRuleState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um valor interpretado como uma combinação de bitmask de sinalizadores que especificam o estado da regra.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULE_STATE  <br/> |
|Identificador:  <br/> |0x6677  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Regras do lado servidor  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir define os possíveis valores dessa propriedade.
  
EN (ST_ENABLED, bitmask 0x00000001)
  
> A regra está habilitada para execução. Se esse sinalizador não estiver definida, o servidor deve pular esta regra ao avaliar regras.
    
ER (ST_ERROR, bitmask 0x00000002)
  
> O servidor encontrou um erro ao processar a regra.
    
DE bitmask 0x00000004 (ST_ONLY_WHEN_OOF)
  
> A regra é executada somente quando o usuário define o estado de fora do escritório (OOF) na caixa de correio. Esse sinalizador não deve ser definida em uma regra de pasta pública.
    
HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)
  
> Esse sinalizador não deve ser definida em uma regra de pasta pública.
    
EL (ST_EXIT_LEVEL, bitmask 0x00000010)
  
> Avaliação de regra será finalizado depois de executar essa regra, exceto para a avaliação das regras de ausência temporária.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)
  
> Avaliação desta regra poderão ser ignorada.
    
PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)
  
> O servidor encontrou um erro ao analisar os dados da regra fornecidos pelo cliente.
    
X
  
> Não usada por esse protocolo. Esse bit não deve ser modificado pelo cliente.
    
Nota sobre a interação entre ST_ONLY_WHEN_OOF e ST_EXIT_LEVEL sinalizadores: 
  
Quando o estado de "ausência temporária" é definido na caixa de correio e uma condição de regra é avaliada como TRUE, 
  
E:
  
- A regra tem o sinalizador ST_EXIT_LEVEL definido e não tem sinalizador ST_ONLY_WHEN_OOF definido. Em seguida, o servidor não deve resultar em regras subsequentes que não tenham ST_ONLY_WHEN_OOF sinalizador será definido e deve ser avaliada regras subsequentes que possuem o sinalizador ST_ONLY_WHEN_OOF definido.
    
OR:
  
- A regra tem os ST_EXIT_LEVEL ST_ONLY_WHEN_OOF sinalizadores e definir. Em seguida, o servidor não deve resultar em quaisquer regras subsequentes.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
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

