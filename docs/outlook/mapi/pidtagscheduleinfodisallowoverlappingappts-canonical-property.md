---
title: Propriedade canônica PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330083"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a>Propriedade canônica PidTagScheduleInfoDisallowOverlappingAppts

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se os compromissos sobrepostos não forem permitidos.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS  <br/> |
|Identificador:  <br/> |0x686F  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade só será significativa quando o valor da propriedade **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PIDTAGSCHEDULEINFOAUTOACCEPTAPPOINTMENTS](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) for true. Um valor TRUE indica que, quando responder automaticamente às solicitações de reunião, um cliente ou servidor deve recusar instâncias que sobrepõem eventos agendados anteriormente. Um valor FALSE ou a ausência dessa propriedade indica que as instâncias de sobreposição devem ser aceitas. Essa não é uma propriedade obrigatória.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
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

