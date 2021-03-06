---
title: Propriedade canônica PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359756"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propriedade canônica PidTagScheduleInfoMonthsTentative

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os meses marcados como provisórios na mensagem de livre/ocupado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificador:  <br/> |0x6851  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Livre/Ocupado  <br/> |
   
## <a name="remarks"></a>Comentários

O número de valores nesta propriedade deve estar entre zero e o número de meses cobertos pelo intervalo de publicação, que é o período entre as propriedades **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) e **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) .
  
Cada valor nessa propriedade tem um mês e um ano codificados nele. Isso é calculado usando a expressão "ano × 16 + mês" onde ano e mês são baseados no calendário gregoriano. Os valores são organizados em ordem crescente e codificados no formato little-endian. Se um evento for espalhado por vários meses ou vários anos, deverá haver um valor para cada um dos meses que se enquadram no intervalo de publicação. Se não houver eventos provisórios no intervalo de publicação, essa propriedade e **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) não devem ser definidos ou devem ser excluídos se já existirem. Caso contrário, essa propriedade deverá ser definida.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
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

