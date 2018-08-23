---
title: Propriedade canônica PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b943f9a3b6f63f185a1b44cfa811d010a287a3d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565813"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Propriedade canônica PidTagScheduleInfoFreeBusyTentative

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os blocos de vezes para o qual o status livre/ocupado é provisório.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Identificador:  <br/> |0x6852  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Informações de disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade tem quantos valores conforme o número de valores no **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Cada valor binário representa um mês e corresponde ao valor no mesmo índice no **PR_SCHDINFO_MONTHS_TENTATIVE**. Os valores binários são classificados na mesma ordem como os valores no **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Cada valor binário tem um ou mais blocos de 4 bytes, e cada um deles contém nos primeiros dois bytes, a hora de início e hora de término nos dois bytes segundo no formato pouco-endian. A hora de início é o número de minutos entre meia-noite Tempo Universal Coordenado (UTC) do primeiro dia do mês e a hora de início do evento em UTC. A hora de término é o número de minutos entre meia-noite UTC do primeiro dia do mês e a hora de término do evento em UTC. Os blocos de 4 bytes são classificados em ordem crescente.
  
Blocos consecutivos ou sobreposição de tempo são mesclados em um bloco com a hora de início como a hora de início do primeiro bloco e hora de término, como o bloco de última hora de término. Se um evento é espalhado por vários meses ou anos, o evento é dividido em vários blocos, um para cada mês. Se não houver nenhum evento provisório do intervalo de publicação, esta propriedade e **PR_SCHDINFO_MONTHS_TENTATIVE** não devem ser definido ou devem ser excluídos se eles já existirem. Caso contrário, essa propriedade deverá ser definida. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
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

