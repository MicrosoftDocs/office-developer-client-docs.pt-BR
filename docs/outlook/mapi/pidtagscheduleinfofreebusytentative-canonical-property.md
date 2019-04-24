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
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359770"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Propriedade canônica PidTagScheduleInfoFreeBusyTentative

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os blocos de horários nos quais o status de disponibilidade é provisório.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Identificador:  <br/> |0x6852  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade tem quantos valores como o número de valores em **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Cada valor binário representa um mês e corresponde ao valor no mesmo índice em **PR_SCHDINFO_MONTHS_TENTATIVE**. Os valores binários são classificados na mesma ordem que os valores em **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Cada valor binário tem um ou mais blocos de 4 bytes, e cada um deles contém a hora de início nos primeiros dois bytes e hora de término nos dois bytes de segundo no formato little-endian. O horário de início é o número de minutos entre o UTC (tempo Universal Coordenado) do primeiro dia do mês e a hora de início do evento em UTC. O horário de término é o número de minutos entre a meia-noite UTC do primeiro dia do mês e a hora de término do evento em UTC. Os blocos de 4 bytes são classificados em ordem crescente.
  
Blocos de tempo consecutivos ou sobrepostos são mesclados em um bloco com hora de início como a hora de início do primeiro bloco e hora de término como a hora de término do último bloco. Se um evento for distribuído por vários meses ou anos, o evento será dividido em vários blocos, um para cada mês. Se não houver eventos provisórios no intervalo de publicação, esta propriedade e **PR_SCHDINFO_MONTHS_TENTATIVE** não devem ser definidas ou devem ser excluídas, caso já existam. Caso contrário, essa propriedade deve ser definida. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
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

